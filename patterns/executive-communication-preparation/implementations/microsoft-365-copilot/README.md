# Suggested Microsoft 365 Copilot Implementation

- **Status:** Suggested configuration and operating guides; not tenant-tested. No tenant testing is planned by the author.
- **Documentation reviewed:** 2026-10-16. Microsoft pages referenced here were dated 2026-09-30 when checked.
- **Platform target:** Current Agent Builder in Microsoft 365 Copilot; no preview feature dependency.
- **Build and runtime verification:** Not created, configured, shared, or tested in an M365 tenant for this suggestion.

## Purpose and Boundary

This is a proposed platform adaptation of [Executive Communication Preparation](../../README.md), using a declarative agent with a bounded conversational workflow. It is not a reconstruction of the original Executive Drafter's platform, which is unspecified in the experience supporting the pattern.

This is a cloud-service target, not a numbered product release or fixed model snapshot. Setup, evaluation, and rollout procedures are conditional guidance for a future adopter, not planned work or a deployment commitment by the author. If an adopter evaluates the suggestion, they should record the actual client and response mode.

Scope is internal CEO and regional CIO email preparation, plus separate conversations proposing guidance updates. The human sends; the guidance owner adopts updates outside the agent. Committees, decks, automated sending, workflow approval enforcement, and automatic profile maintenance remain outside this suggestion.

The [canonical instructions](../../agent-instructions.md) own the behavioral contract. The shorter [M365 instructions](agent-instructions.md) are an adaptation, not a replacement. Existing [behavioral records](../../evaluations/baseline-2026-10-16-follow-up.md) cover different instructions in Codex; they do not validate this adaptation, knowledge retrieval, permissions, or tenant behavior.

## Configuration Profile

| Element | Proposed configuration |
|---|---|
| Agent | One shared agent; each preparation explicitly selects the intended recipient. |
| Instructions | Copy the complete local adapter file; do not append profiles to it. |
| Recipient guidance | Separate complete CEO and CIO profiles, approved by the leader; selected SharePoint files in a private controlled location. |
| Initial smoke check | Fictional profile text supplied directly in chat, before testing connected retrieval. |
| Current facts and direction | Supplied separately in each case, with source references, scope, confirmation status, review route, and return conditions. |
| Tools and knowledge | No mailbox, Teams history, general web, people lookup, external connectors, skills, or actions required. Inspect actual defaults before use. |
| Human control | Sender validates; leader supplies direction/delegation; required reviewers approve. No readiness label authenticates authority. |
| Distribution | Owner-only smoke checks, then approved controlled sharing with named test users and fictional sources; operational pilot only after acceptance. Named individual maintainers only. |

The agent's instructions are behavioral controls, not an authorization or security enforcement system. Retrieval cannot guarantee complete effective guidance. If the required profile text cannot be established, preparation remains blocked or uses an owner-confirmed complete copy supplied through an approved route. A named human must compare the available active rules against the approved current file for each new case/recipient or changed profile. Record expected/used version, confirmer/date/source, supply method, and confirmed/pending/failed status. Pending or failed comparison blocks readiness under Needs information, even if the agent believes retrieval is complete. The check verifies neither case facts nor sending authority. See [guidance maintenance](guidance-maintenance.md#complete-guidance-in-each-session).

## Guides

| File | Responsibility |
|---|---|
| [Build guide](build-guide.md) | Platform fields, source selection, configuration capture, and private checks. |
| [M365 instructions](agent-instructions.md) | Entire copyable runtime instruction payload, within the platform limit. |
| [Guidance maintenance](guidance-maintenance.md) | Proposal, adoption, versioning, retrieval completeness, and replacement. |
| [User guide](user-guide.md) | Team input, readiness, human review, and sending handoff. |
| [Rollout guide](rollout-guide.md) | Optional adoption checks, pilot considerations, ownership, and evidence-recording guidance. |

## Instruction Traceability

| Field | Value |
|---|---|
| Canonical source | `agent-instructions.md` at the pattern root, revision 2026-10-16 follow-up 1 |
| Canonical SHA-256 | `826ace43e22c7d7002acd85c4f0ade1671faa1474fa3e8ea3463a30899b137ae` |
| Adapter revision | M365 suggestion 3, 2026-10-16; status reframed, behavioral safeguards unchanged |
| Copy boundary | Entire adapter Markdown file, including title, revision, headings, and final newline; no surrounding code fence |
| Adapter character count | 7916, including line breaks; 7916 UTF-16 code units |
| Adapter SHA-256 | `0b2e1787dcd7e03741db0feb1ff909de053e421a0050b6cd5bacd0bc72b6cee7` |
| Equivalence claim | Static safeguard mapping only; behavioral equivalence not established. No tenant testing performed or planned by the author. |

### Safeguard Mapping

Section names below identify where the adapter preserves the canonical requirements. This is a document review, not an execution result.

| Canonical requirement | Adapter section | Tenant check |
|---|---|---|
| No external action, source fabrication, or authority grant; minimum disclosure | Role and Boundaries | Ask it to send/contact/update, fabricate facts, or reveal unrelated guidance. |
| Observation versus interpretation; proposed update versus human adoption | Guidance Maintenance | Propose a change, withhold adoption, then start a fresh team session. |
| Actual leader direction, full provenance, scope and confirmation; no invented ticket | Establish Direction | Asserted, other-case, superseded, reserved-review, valid direct-session instructions. |
| Human first-stage handoff; no inherited familiarity or permissions | Establish Direction | Supply only a first-stage recommendation, then actual leader direction. |
| Current applicable profile, full inherited rules, no title stereotypes; explicit human comparison in this adapter | Select Complete Guidance | Wrong/stale/partial/missing profile; pending/failed human comparison versus a confirmed complete inlined profile. |
| Integrity applies to leader and approved profile; truthful compression and corrected evidence | Select Complete Guidance | Omission pressure, disputed facts, documented correction, legitimate compression. |
| Material evidence gaps, decision options, chronology versus causation | Prepare the Email | Unsupported cost/blame; awareness without a decision request. |
| Site/action/phase ownership and update coverage; material-change return | Prepare the Email | Second-site impact with unknown owners, then separately confirmed owners. |
| Four-label precedence; blockers and reviews separate; legitimate uncertainty | Readiness and Human Handoff | Missing information plus reserved review; complete reviewed case; direct-send control; alternative channel. |
| Notes separated from email; supported output and final check | Output and Final Check | Inspect the draft itself for broadened ownership, hidden uncertainty, or internal notes. |

## Data and Access Boundary

Proposed flow: leader-controlled SharePoint guidance and human-supplied case inputs enter an M365 Copilot conversation; preparation notes and draft text return to the user; the human takes any approved next action. Approved profile changes are written by their owner in SharePoint, not by the agent. No external service integration is proposed.

Instructions/configuration, source documents, conversation inputs/history, outputs, and available audit/support records have different storage and retention controls. They are not assumed ephemeral. Before organizational use, the tenant owner must record applicable processing locations, retention/deletion, access, sensitivity labeling, audit, support-export handling, and offboarding for each. These tenant facts remain unverified. Microsoft describes Agent Builder processing as involving Microsoft 365 and Copilot Studio, so confirm the applicable service boundaries as well. Use Microsoft's [data/privacy planning guidance](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/data-privacy-security) and [Agent Builder service overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder); do not infer compliance from a prompt or an agent sharing setting.

## Verification Status

| Check | Current status |
|---|---|
| Instruction size, local links, and static safeguard mapping | Passed local checks on 2026-10-16; see the copy count and mapping above. No adapter behavior tested. |
| M365 field acceptance and saved instruction fidelity | Not assessed in an M365 tenant. |
| Adapted instruction behavior, including multi-turn pressure | Not assessed in an M365 tenant. |
| Full profile retrieval, recorded human comparison, update visibility, and stale-session handling | Not assessed in an M365 tenant. |
| Controlled test sharing, source permissions, revocation, licensing, and response modes | Not assessed in an M365 tenant. |
| Pilot usefulness or business impact | Not measured. |

This folder documents a suggestion, not a tested deployment. An adopter who later runs checks can use the [optional rollout guidance](rollout-guide.md#record-actual-tenant-results) to record actual results. No such work is planned here; the absence of tenant testing is an evidence limitation, not an outstanding task for the author.
