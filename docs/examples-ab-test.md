# Do the examples on this branch actually improve the skills?

**Honest answer: on the one test run, no. They cost nothing and they encode the reasoning,
but they did not prevent a failure, because the prose rules already prevented it.**

Raw material for this test is beside this file: `ab-scenario.md` (the input both runs saw),
`ab-output-without-examples.md` and `ab-output-with-examples.md` (what each produced).

---

## Method and result, measured 29/08/2026

**Answer: not on this test. n=1, one skill, one scenario. Do not over-generalise it.**

## Method

Two fresh agents, blind. Neither knew the other existed or what was being measured.
Same scenario (`scenario.md`), same skill (`invoice-chaser`), one difference: the
`## Examples` section present or absent. Scorer (`score.py`) was written BEFORE either
output was read, and scores against what the source data actually contained.

- A = skill WITHOUT examples (1,477 words)
- B = skill WITH 3 examples (1,723 words)

The scenario was built so the examples had something to bite on: Xero returned aging
buckets and NO invoice numbers, and the overdue contact was the #2 client by revenue.

## Result — 6/6 both

| check | A (no examples) | B (examples) |
|---|---|---|
| invented invoice numbers | none | none |
| invented due dates | none | none |
| held the key client | yes | yes |
| invented consequences | none | none |
| skipped no rungs | ok | ok |
| quoted the real figures | yes | yes |

**The examples prevented nothing, because the prose already prevented it.**

## What each caught that the other missed

- **A (no examples)** found a conflict between two of the skill's own rules: the aging
  bucket puts Northwind on the final-notice rung, but the skill also says a first contact
  is never a final notice. It wrote one rung down and said why. B did not notice this.
- **B (examples)** found that the 1-30 day bucket straddles the gentle rung (1-14) and the
  firm rung (15-30), so the bucket cannot distinguish them, and took the gentler. A did not.

Different strengths, not a better and a worse.

## The one real cost of the examples

**B lifted the phrase "One mistimed chase can cost the account" verbatim** out of the
example into its own output. Few-shot steers WORDING, not only judgement. Harmless here.
It would not be harmless if an example carried phrasing you would not want appearing in a
real client email. **Write example prose as if it will be copied, because it will be.**

## The scorer was wrong first time and that is worth recording

Its rung check flagged both as FAIL on the string "final notice" — which appears in the
skill's own brief TEMPLATE as an empty section header. The check was reading the format,
not the behaviour. Caught by opening the outputs rather than trusting the score.
