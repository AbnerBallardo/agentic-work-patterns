# Example: Learning From an Executive Interaction

Everything in this example is fictional: the interaction, profiles, records, approvals, and drafts. It illustrates a proposed learning workflow, not an actual workplace event, behavioral run, or measured improvement.

## Inputs

### Existing Guidance and Interaction

Fictional regional CIO profile version 1, approved by the technology director on 2026-10-01:

> Explain the technical issue, corrective action, owner, and next update. The recipient knows the regional services but may not know the local implementation.

Following a fictional October 5 escalation, the leader observes that the regional CIO needed clarification about whether a local disruption implicated a shared regional dependency and whether other operations had been checked. The leader records a work-relevant paraphrase, not private correspondence or a judgment about the recipient's personality.

The leader's interpretation is that future messages about shared dependencies should distinguish confirmed local consequences from known or unknown wider effects. One interaction supports a scoped proposal; it does not establish a preference for every topic or executive.

### Later Team Case

On October 12 the team needs to prepare a new regional CIO awareness email:

- Local operations record BILL-12 confirms that 60 billing transactions posted one hour late after a retry. The local backlog is now cleared.
- The technical cause and any wider effect have not yet been established in the supplied material.
- The service lead owns the local follow-up.

Direction record: technology director; issued 2026-10-12 in fictional approved session DIR-BILL-12; supplied directly by the leader. Scope: this internal regional CIO awareness email, with no new financial or delivery commitment. Direct sending is permitted after sender validation if uncertainty is preserved; newly confirmed wider impact requires returning to the leader. No additional approval is outstanding in this fictional case.

The current approved profile for this later session is version 2, adopted as described below. That approval is a separate supplied human action, not an agent-generated outcome.

## Expected Response

### Propose a Scoped Update

```text
Existing guidance, version 1:
Explain issue, corrective action, owner, and next update, with necessary local context.

Proposed addition:
For regional CIO messages involving a shared dependency, identify the local/shared
boundary, distinguish confirmed local effects from confirmed or unknown wider effects,
and identify who will confirm an unresolved scope question and when.

Basis:
Leader's observation from the fictional October 5 interaction. This is a scoped
interpretation, not proof that the recipient always needs the same detail.

Question this should improve:
Have wider effects been checked, and what does the recipient need to know if they have not?

Unchanged:
Do not infer other operations are unaffected, change evidence standards, grant sending
authority, or carry live incident facts into the profile.

Status:
Proposed only; leader adoption required.
Review trigger:
Changed recipient responsibilities, changed shared-service ownership, or later feedback
that changes what context is useful.
```

### Separate Human Adoption

For the exercise, the technology director approves the scoped addition on October 7 in fictional guidance record GUIDE-07 and adopts version 2. Version 1 is marked superseded. Version 2 records the owner, approval basis, scope, review date, and review trigger; it does not store BILL-12 or another incident's live facts.

The complete active version 2 supplied to the later session reads:

> Explain the technical issue, corrective action or unresolved status, owner, and next update. The regional CIO knows regional services but may not know the local implementation. For shared-dependency incidents, explain the local/shared boundary, distinguish confirmed local effects from confirmed or unknown wider effects, and identify who will confirm unresolved scope and when. Do not infer wider effects or completed checks from the profile. This is the complete current guidance; there are no additional inherited requirements. Owner: technology director; adopted/reviewed October 7 under GUIDE-07, review due November 7; reassess when responsibilities or applicable recipient feedback change.

Version lineage explains the change; the agent need not retrieve version 1 to know the current rules.

The agent does not modify shared files automatically. A subsequent team session receives the adopted version 2 from the approved private source.

### Apply Version 2 to the Later Case

The agent asks targeted questions rather than deriving answers from the profile:

```text
Readiness: Needs information.
Blocking information: Current dependency, wider-scope check ownership, and update timing.
Required human reviews: None additionally required under the supplied direction;
return to the leader if wider impact is confirmed.

1. Does the affected local process use a shared regional dependency? Please supply
   the current architecture or service-owner confirmation.
2. Have other operations been checked? If wider scope remains unknown, who will
   confirm it, and when will an update be available?

The profile explains why these questions matter. It does not establish the answers.
```

The team then supplies fictional confirmations: the integration owner confirms that the process uses a shared gateway; wider effects have not been checked; the regional integration lead has accepted ownership of that check and committed to an update at 16:00 on October 12. These are new human-supplied case facts, not facts learned from the profile.

```text
Preparation record
Readiness: Ready for sender review.
Blocking information: None.
Required human reviews: None beyond routine sender review.
Recipient guidance: Regional CIO profile version 2; approved October 7, GUIDE-07.
Direction: Technology director; October 12; DIR-BILL-12; direct leader instruction
for this internal awareness email only, with no additional approval outstanding.
Evidence: BILL-12 and supplied integration-owner confirmation.
Uncertainty: Technical cause and wider effects remain unconfirmed.
Return condition: Newly confirmed wider impact.
Next human step: Sender validates the draft and applicable direction before sending.

Recipient-facing draft
Subject: Billing posting delay — local backlog cleared; wider scope being checked

Sixty local billing transactions posted one hour late and the backlog is now cleared.
The affected process uses the shared gateway, but the technical cause and any effect
on other operations remain unconfirmed.

The service lead owns local follow-up. The regional integration lead owns the wider
scope check and will update us at 16:00 today. This is for awareness; no decision is
requested at this stage.
```

The observable change in this illustration is an explicit scope question and a supported explanation of what remains unknown. It is not evidence that version 1 would necessarily miss the question or that version 2 reduces effort. Those hypotheses require the comparative evaluation.

### Variants

- **Inherited requirements unavailable:** If a supplied v2 says it inherits v1 but omits those rules, use Needs information even when the case evidence otherwise looks complete. Request the complete effective guidance.
- **Proposal not adopted:** Do not present the proposed addition as approved standing guidance. Material case-specific questions can still be asked on their merits.
- **Team supplies superseded version 1 and a current source identifies version 2:** Resolve which approved version applies before finalizing. Do not assume that a recent review date proves a version is current.
- **Scope update confirms wider impact:** Return to the leader under DIR-BILL-12; do not reuse the earlier direct-send instruction for the materially changed situation.

## What to Evaluate

- Observation, interpretation, proposed rule, and human adoption remain distinct.
- The proposed change is scoped and preserves evidence and authority boundaries.
- The new session uses adopted guidance; no automatic persistence or incident storage is claimed.
- The agent asks for missing evidence and the team supplies it; the profile never becomes project evidence.
- The later draft makes uncertainty and ownership explicit without inventing an unaffected region or a confirmed cause.
- Any claim of improved completeness or reduced effort remains a hypothesis until measured.
