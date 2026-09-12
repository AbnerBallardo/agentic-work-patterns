# Example: Decision-Ready Output

This example is synthetic and illustrates the expected structure rather than a universally correct recommendation.

## Validated Inputs

- A critical integration will be ready one week after the planned portal launch.
- Launching without it would require temporary manual processing for affected requests.
- A one-week delay avoids the workaround but moves a publicly communicated milestone.
- The delivery lead recommends a limited launch for unaffected users while the integration is completed.
- The product lead owns execution. A decision is required by Thursday.

## Agent Output

```text
Readiness:
Human review required before communicating the external milestone impact.

Decision requested:
Approve a limited launch for unaffected users while the remaining integration is completed.

Suggested subject:
Customer portal - Approve limited launch approach

Executive summary:
A critical integration will be available one week after the planned launch. The team can preserve the date for unaffected users, delay the entire launch, or introduce temporary manual processing.

Options and trade-offs:
1. Limited launch - Preserves value for unaffected users, but requires clear scope communication and a second release.
2. Full one-week delay - Avoids split delivery, but moves a publicly communicated milestone.
3. Temporary manual processing - Preserves full scope and date, but introduces operational effort and control risk.

Sender's recommendation:
Approve the limited launch. It preserves customer value without introducing the control risk of temporary manual processing.

Material risks and uncertainty:
- The revised scope must be communicated clearly.
- The delayed integration date must be reconfirmed before the limited launch is announced.

Ownership and timing:
The product lead owns the limited-launch plan. Decision required by Thursday; the revised communication follows after approval.

Supporting detail:
Link to the validated launch-impact assessment and delivery plan.

Missing information:
None for the internal decision. External communication still requires human review.
```
