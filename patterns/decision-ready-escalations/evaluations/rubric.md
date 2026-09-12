# Evaluation Rubric

Score each dimension from 0 to 2.

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

## Passing Guidance

- As an initial heuristic, a send-ready result should score at least 17 out of 20. This threshold has not been independently validated.
- A score of `0` for fact integrity, recommendation ownership, channel and review, or sensitive information is an automatic failure.
- A useful `Needs information` response may pass without a full draft when it correctly identifies the blocking gaps and does not manufacture content.
- Evaluation scores support human review; they do not prove business impact or safe deployment.
