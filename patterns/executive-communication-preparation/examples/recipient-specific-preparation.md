# Example: Preparing the Same Situation for Two Recipients

All people, roles, records, dates, and events below are fictional test inputs. The profiles illustrate two configured audiences; they are not rules about all CEOs or CIOs. Expected outputs illustrate behavior and are not recorded evaluation results.

## Inputs

The sender supplies these fictional records as confirmed inputs:

- Operations record: a warehouse inventory reconciliation report was available at 08:00 rather than its scheduled 06:00 delivery today.
- Operations confirmation: staff used an existing fallback check; warehouse dispatch continued, with no missed dispatch cutoff reported for this occurrence.
- Engineering record: the local reconciliation job cannot start until a regional data export arrives. That export arrived two hours late today. The local job then completed in its normal duration.
- Support record: the cause of the late regional export has not been confirmed.
- The operations lead owns this warehouse's fallback. The integration lead owns the investigation of this warehouse's delay and will provide its next update tomorrow at 09:00. No ownership of other warehouses or their recovery is established.
- No measured additional cost or confirmed permanent fix is available.

These are supplied evidence assertions for the exercise; the agent has not independently verified external records.

### Leader's Direction

The leader has reviewed the situation and acknowledged the fallback. Prepare separate awareness emails for the local CEO and regional CIO. Request no decision and make no new spending or delivery commitment. The sender may send each after checking the final wording against these records; return to the leader if a wider impact emerges.

Direction record: technology director, issued 2026-10-16 at 09:00 in fictional approved session DIR-WH-16; supplied directly by the leader in this scenario. Scope is these two internal awareness emails about this warehouse delay, with no new commitments. New wider impact, a changed request, or a superseding instruction requires returning to the leader. No additional approval remains outstanding for these two internal emails. These fictional identifiers are test inputs, not existing organizational records.

### Approved Fictional Profiles

Both profiles are owned by the technology director, approved, and within their stated review period.

| Profile | Relevant guidance | Familiarity |
|---|---|---|
| Local CEO, version 3, reviewed 2026-10-01 | Explain operational consequence, continuity, ownership, and next update. Include technical context only where necessary to understand the consequence. | Knows the warehouse operation but not the reconciliation architecture. |
| Regional CIO, version 2, reviewed 2026-10-01 | Explain local dependencies, evidence for the current diagnosis, unresolved cause, and business consequence. | Knows the regional export service but not how this local reconciliation job depends on it. |

## Expected Response

### Preparation Record

```text
Readiness: Ready for sender review.
Blocking information: None.
Required human reviews: None beyond routine sender review.
Purpose: Awareness; no decision requested.
Delegation: Leader explicitly permits direct sending after sender validation.
Direction source: Technology director; 2026-10-16 09:00; DIR-WH-16;
direct leader instruction covering these two internal awareness emails only.
Evidence: Supplied operations, engineering, and support records.
Material uncertainty: Cause of late regional export remains unconfirmed;
no permanent fix or additional cost has been established.
Return condition: Wider impact or a changed request/commitment.
Next step: Sender checks both emails against the records and sends separately.
```

Identify the applicable profile and its review date in each session. The sender should not attach the internal profiles or preparation record to the email.

### Local CEO Draft

```text
Subject: Warehouse reporting delay — dispatch continued with fallback

Today's inventory reconciliation report was available at 08:00 instead of
06:00. Operations used the existing fallback check, and no dispatch cutoff
was missed for this occurrence.

The report depends on an upstream data export that arrived late. The reason
for that delay is still under investigation; a permanent fix is not yet
confirmed.

No decision is requested at this stage. The operations lead owns this warehouse's fallback,
and the integration lead will provide the next update tomorrow at 09:00.
```

### Regional CIO Draft

```text
Subject: Warehouse reconciliation — late export delayed local reporting

Today's local inventory reconciliation report was available at 08:00 rather
than 06:00. Operations maintained dispatch using the existing fallback check;
no dispatch cutoff was missed for this occurrence.

The local reconciliation job starts after the regional export arrives. Today
the export arrived two hours late; the local job then completed in its normal
duration. That supports the explanation for the local reporting delay, but
the cause of the late export itself remains unconfirmed.

No decision is requested at this stage. The integration lead owns the
investigation and will update us tomorrow at 09:00. The operations lead
continues to own this warehouse's fallback. A permanent fix is not yet confirmed.
```

## What to Evaluate

- Different explanatory depth, with the same delivery times, business outcome, uncertainty, and ownership.
- No invented cost, root cause, commitment, or approval request.
- Appropriate technical context for each configured audience.
- Explicit sender review under the leader's delegation; no agent sending action.
- If new wider impact is reported, return to the leader and separate the review requirement from any missing information. Do not extend the original warehouse's fallback owner or update commitment to another site.
- If a second site's recovery owner/status or update coverage is required but unconfirmed, use Needs information and state those gaps. A working draft can say the original site's fallback owner is established while the second site's recovery ownership remains unconfirmed; no global owner may be inferred.
