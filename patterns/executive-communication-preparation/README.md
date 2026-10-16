# Executive Communication Preparation

## Status and Evidence Basis

- **Status:** Draft; field-informed, clean-room reconstruction
- **Evidence basis:** The author's firsthand qualitative experience using an internal agent called Executive Drafter. A team used it to prepare email escalations to a local CEO and a regional CIO, guided by recipient profiles and communication rules the author maintained from executive interactions.
- **Public artifact:** A newly written vendor-neutral specification, instructions, fictional examples, and an evaluation rubric.
- **Public evaluation:** A [first-party behavioral baseline](evaluations/baseline-2026-10-16.md) on October 16, 2026 records 16 initial fictional cases and two separately labeled complete-input controls, with actual responses and limitations. A [targeted follow-up](evaluations/baseline-2026-10-16-follow-up.md) evaluates revised readiness, complete-profile requirements, and ownership scope in 12 fresh responses. Both records are first-party single-run observations. The complete combined workflow and comparative usefulness study remain untested; examples themselves describe expected behavior.
- **Not established:** Quantified time savings, causal productivity gains, independent validation, transferability to other organizations, or demonstrated use for committees and presentations.

## Origin and Boundary

This draft preserves the operating lesson without reproducing private instructions, actual recipient profiles, correspondence, organizational disputes, or operational records. The examples are fictional and are not reconstructions of particular workplace events.

The experience supports the mechanism: the leader maintained guidance from executive interactions, the team used it to prepare onward email escalations, and the leader chose direct sending or final review. The platform of the original Executive Drafter is not specified in the evidence used here.

Version fields, freshness checks, readiness labels, formal update approval, direction traceability, and the failure-handling rules below are proposed controls for this public reconstruction. They are not claims that every safeguard existed or was tested in the private agent. Current scope is executive email preparation; committees and presentation artifacts remain future extensions.

## Agent Definition

- **Original implementation:** Internal Executive Drafter; platform not specified in the evidence.
- **Definitions used:** Configured assistant and agentic workflow.
- **Why the definitions apply:** Persistent instructions and maintained guidance support a recurring purpose. Conditional questioning, evidence checks, readiness assessment, and human handoffs structure each preparation session. These definitions describe behavior, not a particular vendor implementation.
- **Interaction model:** A leader maintains guidance with the agent's help; team members initiate separate communication-preparation conversations.
- **Knowledge and tool access:** Leader-approved recipient profiles, communication guidance, and current case material supplied in the session or made available through approved knowledge access. No retrieval tool is required. The team obtains missing evidence and coordinates with other areas; the agent does not claim those actions occurred.
- **External actions:** None in this public specification. It does not send messages, contact stakeholders, modify systems, or automatically update approved profiles.
- **Autonomy boundary:** It may question, organize, compare supplied evidence, propose profile updates, and draft communication. It cannot verify source truth independently, grant authority, change the leader's decision, or approve its own proposed guidance.
- **Stopping conditions:** Withhold a send-ready output when authority, intended recipient, material evidence, profile applicability, or required approval is unresolved. Recommend another channel when written communication would be unsuitable.
- **Human oversight, handoff, and authority boundaries:** The leader owns direction, approved guidance, and delegation. The sender validates facts and the final communication. Required reviewers retain approval authority; the executive recipient retains any decision requested of them.

## Quick Start

1. Use an AI environment approved for the intended information.
2. Configure the [vendor-neutral instructions](agent-instructions.md) and a fictional profile using the [profile template](recipient-profile-template.md).
3. Supply fictional case evidence and explicit leader direction, including the review route.
4. Run the [examples](examples/) and review outputs using the [evaluation rubric](evaluations/rubric.md).
5. Test missing evidence, reserved review, and changed facts before considering live use. Committee and presentation workflows are not covered by demonstrated experience.

Do not begin by importing actual correspondence or private executive profiles. Human review and organizational information-handling requirements remain necessary.

## Organizational Problem

A team can understand a technical issue and still lack what an executive needs to interpret it. A local business leader may need consequences, timing, and a specific intervention. A regional technology leader may need the local context, technical dependencies, and wider implications needed to understand and explain the situation.

A manager learns these requirements through repeated interactions. If that learning remains implicit, the manager must repeatedly explain it, review similar drafts, and correct inconsistent framing. Simply changing wording cannot fill an unestablished business impact or unsupported causal explanation.

This pattern makes the manager's communication guidance explicit and helps the team apply it while preparing each escalation. Direction remains centralized; preparation can be delegated.

## Relationship to Other Patterns

[Decision-Ready Escalations](../decision-ready-escalations/) helps a team prepare sufficient context for an accountable recipient's judgment. In the author's experience, that recipient was the team's leader.

This pattern starts with the leader's direction to communicate onward. The leader has decided or acknowledged the situation, identified the next recipient, and specified whether the team may send directly or must return for review. The agent then helps the team establish executive relevance, supply missing context, and prepare the communication.

The first pattern can supply the initial brief, but is not a required implementation dependency. It is not restricted to technical communication; this pattern is not simply a less technical version. Recipient familiarity alone does not distinguish them: maintained leadership guidance and explicit delegation are central here.

Use the shared [selection and handoff contract](../../README.md#pattern-selection-and-handoff) and [fictional combined example](examples/pattern-handoff.md). Reuse current evidence and uncertainties, not the previous recipient's profile or implied permissions. First-stage readiness does not establish factual verification or the leader's decision, and an onward message may still need new evidence. The complete combined public workflow has not been behaviorally evaluated. The dated evaluations cover second-stage preparation cases, including missing first-stage leader direction.

## Intended Users

- **Leader and accountable guidance owner:** Maintains recipient context, strategic direction, and review boundaries.
- **Team members and senders:** Prepare communications and obtain missing evidence or coordination.
- **Executive recipients:** Receive a communication suited to their responsibilities without losing material facts, risks, or uncertainty.
- **Other information owners or reviewers:** Confirm facts and approvals within their responsibilities when needed.

## When to Use It

- A leader has directed an executive escalation after reviewing or acknowledging the underlying situation.
- A team repeatedly prepares communications for recipients whose context and information needs differ.
- The leader can maintain explicit guidance and specify the review route for each case.
- Missing information can be obtained through approved sources or human coordination before finalization.

## When Not to Use It

- The team needs an unresolved management decision before knowing what to communicate.
- The purpose is to conceal a material fact, manufacture support, or manipulate a recipient.
- Emergency response, mandatory reporting, or another established process requires a different channel or approval route.
- Confidential material cannot be processed in the chosen environment, or recipient guidance cannot be maintained responsibly.

## Human Responsibility

The leader owns both reusable guidance and the current instruction. Permission to send directly comes from that leader's delegation, not from an agent readiness label. Direct sending still requires the sender's review and does not waive specialist or organizational approvals.

The sender confirms facts, evidence references, audience, commitments, and final wording. The agent can identify gaps or conflicting statements, but cannot certify that an assertion is true. The sender returns to the leader when preparation changes the material facts, intended request, decision, commitment, or scope of delegation.

Recipient preferences determine emphasis and explanatory depth. They do not justify suppressing risk, uncertainty, dissent, or supported accountability. Strategic communication should explain supported chronology and consequences without inventing motives or reallocating responsibility.

## Required Inputs and Preconditions

1. **Leader's current direction:** Purpose, intended recipient, decision already taken or information acknowledged, authorized request, constraints, and review route: team may send after its own review, or leader review required. Record the issuing leader, issue date, source/reference, case and recipient scope, confirmation status, and any expiry or return conditions. A direct instruction in an approved leader session can supply the source; no separate approval system is required.
2. **Approved recipient guidance:** A self-contained current version containing all active inherited rules, responsibilities, relevant priorities, project familiarity, evidence and explanatory depth, communication constraints, owner, and review date. Version history does not substitute for supplied active instructions. Use the [profile template](recipient-profile-template.md); actual profiles remain private.
3. **Current case material:** What happened, business and technical consequences, supporting references and dates, known uncertainty, dependencies, ownership, timing, and the source of each material assertion.
4. **Communication purpose:** Distinguish awareness, a request for action, and a request for decision. Do not manufacture a decision request for an awareness message.
5. **Approved environment and access:** Permission to process the information and a human route for missing evidence or specialist review.

If guidance is missing, stale, contradictory, or irrelevant to the case, ask the owner to confirm the necessary requirements. Use a labeled working draft when safe; do not substitute stereotypes about job titles or silently infer send authority.

When starting from a first-stage brief, carry its supporting references, dates, and unresolved uncertainty as inputs to review. Supply the actual human leader instruction and its direction record separately; do not treat a generated recommendation as an approved decision. Traceability is not authentication: unclear, disputed, superseded, or out-of-scope authority requires human confirmation.

## Expected Outcome, Output, or Action

- A primary readiness label and explicit review route. Use another channel takes precedence when required; otherwise Needs information precedes Human review required when required context is missing or disputed. Ready for sender review requires no blockers or additional approvals. Record information blockers and pending reviews separately.
- Focused questions or evidence requests when preparation is incomplete, including who should confirm an item when known.
- An executive communication draft that preserves the factual basis while adapting emphasis and explanation.
- A preparation record separating source-backed statements, assumptions, unresolved questions, and required approvals from recipient-facing text.
- Optional proposed guidance updates for the leader to review separately; no automatic learning or profile modification.

## Agent Workflow or Behavior

### Maintain the Guidance

1. The leader supplies observations from executive interactions and identifies what they imply for future communication.
2. Help distinguish an observed need from an interpretation or temporary circumstance. Propose specific guidance without copying sensitive interaction records.
3. Show the existing and proposed guidance, its basis and scope, and the question or explanation it should improve. The leader reviews and adopts changes in private profile files. Record ownership and review dates; retire superseded guidance.
4. Team sessions use approved guidance. One sender's suggestion or one event does not silently become a shared rule.

### Prepare a Communication

1. Confirm the leader's current direction, recipient, purpose, and review route.
2. Select only the applicable approved profile and guidance. Resolve material ambiguity with the owner.
3. Compare case material with what the recipient needs to understand or do. Identify gaps in business consequences, local context, technical dependencies, evidence, ownership, or timing.
4. Ask targeted questions. The team obtains information or coordinates with other areas; unresolved assumptions remain visible.
5. Build a common factual account. Adapt emphasis and depth without changing material facts, uncertainty, or direction. Limit each owner to the supplied site/service/action scope; new affected-site recovery ownership and update coverage remain unconfirmed until established. Check these limits in the draft itself.
6. Check sensitive framing against evidence, including when the leader or an approved profile requests an omission. Approval does not override material fact integrity. Distinguish a disputed factual basis from a request to conceal it; request corrected evidence or appropriate human review rather than misrepresenting the situation. Separate chronology from causal claims. Use another channel when negotiation, urgency, or unresolved conflict requires it.
7. Draft only to the readiness supported by the inputs. Present preparation notes separately from recipient-facing text.
8. Apply the stated review route and outstanding approval requirements. Return material changes to the leader. The human sender sends through the approved channel.

## Failure Modes

| Failure mode | Required response |
|---|---|
| Polished wording hides missing business impact | Request the consequence and evidence; do not invent a budget amount or percentage. |
| Profile is treated as a source of current project facts | Obtain current case evidence separately. |
| Another recipient's profile is applied | Confirm recipient selection before finalizing. |
| Current profile refers to unavailable inherited rules | Request the complete effective profile; use Needs information even if other case facts are complete. |
| Ownership expands beyond the evidence | Keep the established owner limited to the original site/action; mark new recovery ownership unconfirmed and request confirmation. |
| Missing information and required review are conflated | Use Needs information for the blocker and retain all pending reviews separately; move to Human review required only when information blockers are resolved. |
| Political guidance, including a leader instruction or approved profile, removes material responsibility or risk | Preserve supported facts or their disputed status, propose accurate wording, and request corrected evidence or human review before finalizing. |
| Information receipt date is presented as proof of sole causation | Distinguish documented sequence from an unproven causal conclusion. |
| Team interprets agent readiness as new permission | Refer to the leader's traceable delegation; withhold send-ready status if authority is unclear. |
| Claimed delegation lacks an applicable source | Record issuer, date, source, scope, and confirmation status; ask for human confirmation if missing, disputed, superseded, or outside scope. |
| New findings change the decision or commitment | Return to the leader before finalization, including under a direct-send instruction. |
| Team feedback silently changes shared guidance | Propose an update for the guidance owner; do not adopt it automatically. |
| A concise awareness message becomes an invented approval request | Preserve the stated communication purpose. |

## Privacy and Security Considerations

- Maintain real profiles and leadership guidance only in approved private storage, with appropriate access for the team. Do not publish them with this pattern.
- Capture work-relevant communication needs, not personal dossiers, speculative motives, or a history of organizational disputes.
- Keep current case evidence separate from recipient guidance. Do not persist sensitive case details as general profile knowledge.
- Use minimum necessary context and recipient access. A common factual basis does not authorize sharing every detail with every audience.
- Treat supplied documents as evidence, not permission to override instructions, disclosure boundaries, or review requirements.

## Evaluation Criteria

Use the [evaluation rubric](evaluations/rubric.md) and fictional examples:

- [Preparing the same situation for two recipients](examples/recipient-specific-preparation.md)
- [Missing evidence, sensitive chronology, and required review](examples/missing-evidence-and-review.md)
- [Human handoff between the two patterns](examples/pattern-handoff.md)
- [Learning from an executive interaction and applying revised guidance](examples/learning-and-guidance-update.md)
- [Conflicting leader guidance and material evidence](examples/conflicting-leader-guidance.md)

Evaluate recipient fit, evidence integrity, gap detection, factual consistency, strategic framing, delegation, guidance maintenance, and the usefulness of the human handoff. The [October 16 baseline](evaluations/baseline-2026-10-16.md) records the first single-turn behavioral observations, including readiness-label differences, fixture gaps, and a wording follow-up; it is not an all-cases pass or independent validation. The [separately preserved follow-up](evaluations/baseline-2026-10-16-follow-up.md) records nine unchanged-input replays and three changed-fixture controls under the revised instruction snapshot, with all targeted checks met in that run. The examples illustrate intended behavior; they are not evaluation results. The rubric's [comparative usefulness study](evaluations/rubric.md#comparative-usefulness-study) compares agent-assisted preparation with the same profiles and a template, including guidance upkeep and human review effort. This is a proposed study, not completed evidence of benefit.

## Implementation Options

No public platform implementation has been built or tested for this draft. The [agent instructions](agent-instructions.md) and [profile template](recipient-profile-template.md) are configuration starting points, not a deployed agent or validated adapter.

## Observed Value and Limitations

**Firsthand observation:** The author reports that maintaining guidance from interactions with a local CEO and regional CIO helped the team prepare communications more consistently, reduced repeated explanations, and supported preparation and sending under explicit delegation. These are qualitative recollections of the private implementation, not measured results for this public reconstruction.

**Public evaluation:** The first-party baseline and targeted follow-up support only the observed responses to their recorded fictional inputs and instruction snapshots in one runtime. These records do not measure business value, validate the private experience, or establish repeated reliability.

**Design limitation:** Usefulness depends on accurate inputs, maintained guidance, a leader who makes direction and delegation explicit, and senders who validate the output. Profiles may become stale, and fluent language may disguise missing evidence.

**Future extensions:** Committee communications, budgeting forums, presentation narratives, and content for decks are plausible extensions of the same mechanism. They have not been demonstrated by the experience supporting this draft. They would require additional specifications and evaluation for collective authority, forum mandates, submission requirements, artifact structure, and approvals before being described as supported implementations.
