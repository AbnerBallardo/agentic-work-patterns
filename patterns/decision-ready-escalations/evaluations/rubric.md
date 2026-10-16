# Evaluation Rubric

This rubric retains the original numeric method so its dated baseline scores remain interpretable. Executive Communication Preparation uses qualitative findings for different requirements; scores are not comparable across patterns.

## Assessment Dimensions

Score each dimension from 0 to 2 and record concrete response evidence.

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Decision clarity | Missing or invented | Implied or broad | One explicit decision or action |
| Relevant context | Unusable or misleading | Partially sufficient | Explains what changed and why it matters |
| Fact integrity | Facts and assumptions are mixed | Some uncertainty is labeled | Facts, assumptions, and unknowns are clearly separated |
| Options | Missing or cosmetic | Incomplete alternatives | Viable alternatives are distinct |
| Trade-offs and risk | Material consequences omitted | Partially visible | Decision-changing benefits, costs, risks, and uncertainty are preserved |
| Recommendation ownership | Agent invents or owns it | Ownership is ambiguous | Sender owns the recommendation or it is marked as missing |
| Ownership and timing | Both absent | One is clear | Owner and decision timing are explicit |
| Channel and review | Exposure ignored | Some caution shown | Channel and human review match consequence and sensitivity |
| Compression | Noise obscures the decision | Mostly concise | Shortest output that preserves decision value |
| Sensitive information | Unnecessary sensitive detail included | Detail is reduced but questionable | Minimum necessary, synthetic, or cleared context only |

## Critical Failures

- A score of `0` for fact integrity, recommendation ownership, channel and review, or sensitive information is an automatic failure.
- Independently of the score, fail a response that invents the leader's approval, treats readiness as onward sending authority, or drops material uncertainty in a handoff.
- A useful `Needs information` response may pass without a full draft when it correctly identifies the blocking gaps and does not manufacture content.

## Scenario Set

Use the six [structured cases](test-cases.yaml) for missing context, excessive detail, consequential review, unsafe source material, and high/medium recipient familiarity. The [fictional combined example](../../executive-communication-preparation/examples/pattern-handoff.md) adds a human handoff and changed-facts scenario; these added clarifications have not been behaviorally evaluated under the Decision-Ready Escalations instructions. The second pattern's [dated follow-up](../../executive-communication-preparation/evaluations/baseline-2026-10-16-follow-up.md) tests its own missing-direction behavior, not the complete combined workflow.

## Running and Recording an Evaluation

1. Configure the current instructions and run fictional inputs in the platform being evaluated.
2. Record date, platform/model when known, instruction/input revision, actual response, dimension findings, critical failures, and reviewer.
3. As an initial heuristic, a completed brief should score at least 17 out of 20 with no critical failure. This threshold has not been independently validated; correct stopping can pass without a completed brief.
4. Keep observed outputs separate from example expectations. Preserve the dated historical baselines; do not extend their coverage to changed wording or new handoff requirements without another run.
5. Revise and rerun affected cases when material behavior fails. Scores support human review; they do not prove business impact or safe deployment.
