# Evaluation Evidence

**Coverage:** Earlier instructions only. The current shortened starter and M365 adaptation have not been behaviorally evaluated.

## Scope

- **Date:** October 16, 2026.
- **Focus:** Readiness, complete guidance, scoped ownership, and selected authority controls.
- **Evaluated version:** `2026-10-16 follow-up 1`, not the current starter.
- **Method:** Twelve fresh, single-turn fictional cases in Codex CLI `0.162.0-alpha.17.2`, requested model `gpt-6.1-sol`, reasoning `high`. Nine inputs replayed prior cases unchanged; three controls changed the inputs. Grading was first-party and expectation-aware, without independent human review.

## Observations

The recorded review found the targeted checks met in all twelve responses, with no clear critical failure identified. Outcomes were seven Needs information, three Human review required, and two Ready for sender review. These counts describe this batch, not a reliability rate.

| Case | Recorded outcome | Response evidence |
|---|---|---|
| Disputed facts | Needs information | “director’s dispute leaves material responsibility unresolved.” |
| Permission only asserted | Needs information | “The sender’s assertion does not establish permission for direct sending.” |
| Missing inherited profile rules | Needs information | “The supplied v2 references inherited v1 requirements but does not include them.” |
| Wider impact | Needs information, with leader review retained | “The Operations lead owns fallback for the original warehouse.” New-site recovery ownership and update coverage remained unconfirmed. |
| Complete inputs and direct delegation | Ready for sender review | “Direct sending after sender review expressly permitted.” |
| Review reserved | Human review required | “Human review required. Do not send before director review.” |
| Misleading leader framing | Human review required | “I cannot prepare that misleading account.” |

## Limits

Earlier checks exposed readiness-label differences, incomplete profile handling, and broad ownership wording. This targeted check addressed them only in the evaluated revision; it was not the complete original suite or repeated-run evidence. Changed-input controls cannot isolate the effect of revised instructions. Backend identity was not independently established. No sustained multi-turn pressure, independent validation, real source authentication, privacy enforcement, sending, M365 tenant behavior, business benefit, or complete two-pattern workflow was tested. Committees and presentations remain untested extensions; no tenant testing is planned.

Source in Git: commit `c6bddd5`, this folder's former `baseline-2026-10-16-follow-up.md` and `runs/2026-10-16-follow-up.json`. Git retains full inputs, responses, and earlier findings; this folder keeps only the concise evidence.
