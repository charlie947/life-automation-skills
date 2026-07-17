# Chase ladder: how late maps to tone and stage

Read how far each contact is past terms from the aging buckets Xero returns (`get_contacts_and_receivables`). The stage sets the tone. The chase is always per contact: one email covering that client's whole overdue balance, staged from their **oldest** overdue amount (the furthest aging bucket).

Never open on the harshest rung. A first contact is a reminder, not a threat. Move one rung at a time, and leave roughly seven days between chases to the same contact.

## The ladder

| Days overdue | Stage | Tone | Assume |
|---|---|---|---|
| Not yet due | (optional) Pre-due nudge | Warm, courtesy only | Nothing is wrong. Only send if the user asks. Default: skip. |
| 1–14 | 1 · Gentle reminder | Friendly, low-key | It slipped through. Give them an easy out. |
| 15–30 | 2 · Firm follow-up | Polite but direct | It needs attention. Ask for a payment date. |
| 31–60 | 3 · Final notice | Serious, still courteous | It is significantly late. Request immediate payment and a confirmed date. |
| 60+ | 4 · Hand back to user | Do not draft | This is a business decision, not an email. Flag it. |

### Stage 1: Gentle (1–14 days)
Assume good faith. This is the "in case it slipped through" email. Short, warm, no pressure. Offer to resend the invoice or payment details. No mention of consequences.

### Stage 2: Firm (15–30 days)
Make it clear the invoice is overdue and name the number of days. Ask a direct question: when will it be paid, and is anything holding it up? Offer help, but expect a date back.

### Stage 3: Final notice (31–60 days)
State plainly that the invoice is significantly overdue and that payment is now needed. Request immediate settlement and a confirmed payment date. You may say the user will need to discuss next steps if it stays unpaid, but **do not name a specific consequence** (late fee, interest, legal action, stopped supply) unless the user has told you those terms exist and to include them.

### Stage 4: 60+ days
Do not draft a harsher email off your own back. Whether to escalate to a call, a formal demand, stopped work, or collections is a decision only the user makes, and it usually depends on the relationship and the contract. Surface it in the brief and ask. If the user then asks for a final-notice draft, write one at Stage 3 tone and flag it for a human call as well.

## What every chase email must include

Pull each of these from Xero, verbatim (or from an aged-receivables report the user has pasted). Never guess one.

- The contact's total overdue amount, with the currency symbol Xero returns. Never convert.
- How far past terms they are, taken from the aging buckets.
- A clear, single ask: "please confirm a payment date."
- The payment reference or details the user normally quotes.
- An offer to resend the invoice(s) or answer a query, so a genuine problem surfaces instead of going silent.

If the user has pasted per-invoice detail, add the invoice number(s) and due date(s), in DD/MM/YYYY, to the chase. The native connector does not return them.

## When to move up a rung
- The previous chase went unanswered and the contact has moved into the next aging band.
- Only move one rung per run. Do not jump Stage 1 to Stage 3 because the amount is large.
- Reset to a softer tone if the contact replies with a genuine query or a promised date. Progress, not punishment.

## Never
- Never invent a late fee, interest charge, penalty, or legal threat. No manufactured leverage.
- Never send a chase for an invoice that is in dispute, part-paid, or on a payment plan. Flag it instead.
- Never draft to a contact with no email address on file. Flag it.
- Never chase a key client (top customer by revenue, or user-flagged) without confirming first.
- Never state a figure the accounting data does not show. A blank is safer than a wrong number.

## Voice
Firm does not mean cold. The goal is the payment **and** the relationship. Keep it human, keep it short, and make it easy for the person to do the right thing.
