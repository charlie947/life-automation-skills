# Dedupe rules: what counts as a duplicate, who wins, what to fill

The job is to make a contact table clean without ever losing real data or inventing fake data. When in doubt, propose and ask. Never merge or delete silently.

## What counts as a duplicate

Two records are the same person (or the same company) when a strong key matches. Rank matches by confidence, because confidence decides whether they can be batched or must be asked one by one.

### High confidence: same identity, can be batched with one explicit yes
- **Same email**, once normalised: lowercase, trimmed of surrounding spaces. Two records with `A@Firm.com` and `a@firm.com ` are the same person.
- **Same phone**, once normalised to one format (e.g. E.164 `+44…`). `07700 900123` and `+44 7700 900123` are the same.
- **Same record ID pointed at from two rows** (a genuine double entry).

### Low confidence: probably the same, always ask per item
- **Same full name + same company.** Common names collide. Ask.
- **Same name + same email domain** (e.g. two "J. Smith" at `@firm.com`). Could be one person, could be two colleagues. Ask.
- **Very similar names** (typo, initial vs full first name, maiden vs married). Show both and let the user decide.

### Not a duplicate: never merge on these alone
- Same company only. That is a colleague, not a copy.
- Same first name only.
- A shared generic inbox (`info@`, `hello@`, `sales@`). Flag it, do not merge people behind it.
- A plus-tagged Gmail (`name+shop@gmail.com` vs `name@gmail.com`). Often the same person, but treat as low confidence and ask.

## Which record wins on merge (survivorship)

Pick one survivor per group. Work down this order until one record wins:

1. **Most complete.** The record with the most non-empty fields.
2. **Most recently active.** Most recent modified date, last-contacted date, or newest note.
3. **Most connected.** The record linked to live deals, tasks, or notes downstream. Keeping it avoids breaking those links.
4. **Tiebreak: oldest created.** Only to settle a tie, because older records tend to be the canonical ID others point to.

Then merge field by field into the survivor:

- For each field, **keep the non-empty value.** If the survivor's field is blank and the loser's is filled, take the loser's value.
- If both are filled and they **differ**, keep the survivor's value and **preserve the loser's in a note** (e.g. `alt email: …`). Never silently drop a real value.
- **Never overwrite a filled field with a blank.** A merge only ever adds information or moves it into a note.
- Collect linked items (deals, notes, tags) onto the survivor where the connector allows it. Where it cannot relink automatically, list what needs re-pointing so the user can finish it.

Retire the loser only after the survivor is written and confirmed. In Airtable that is a delete (revert undoes only the last action). In Notion there is no delete, so flag the loser (e.g. set a "Merged into →" field) and let the user archive it to Trash in the UI.

## Safe enrichment sources

Fill a blank only from a real, named source. Cite the source in the proposal.

- **Another record in the same base.** The same company already has a filled address on a sister record.
- **A source the user hands you.** A pasted list, a spreadsheet, a page they point to.
- **A public source the user approves**, and only one you can actually see and name (the company's own website for a company field, a public profile the user links). Quote the source, do not paraphrase a memory of it.

Everything else stays blank and is marked `[NEEDS: …]`. A gap the user can see beats a guess they cannot check.

## Never-guess fields

These are never inferred, patterned, or filled from a hunch. If there is no real source, leave blank and mark `[NEEDS: …]`:

- **Email.** Never build one from a `first.last@domain` pattern. A pattern is a guess.
- **Phone number.** Never infer from a country or a colleague.
- **Job title or seniority.** Never assume from a name, a company, or a signature guess.
- **Company or employer** when only a personal email is known.
- **Any personal attribute** (location, pronouns, birthday, anything sensitive).

## Formatting fixes that are safe

Reversible, low-risk tidying can be proposed in a batch:

- Trim leading and trailing whitespace.
- Lowercase email addresses.
- Standardise phone numbers to one chosen format.
- Fix obvious name casing (`JANE DOE` → `Jane Doe`), but leave real mixed case alone (`McDonald`, `de Vries`).
- Standardise a company name to one spelling once the user confirms the canonical form.

Anything ambiguous (which spelling of a company is canonical, whether two names are one person) is flagged for the user, not forced.
