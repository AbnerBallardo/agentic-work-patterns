# Decision-Ready Escalations

## Status and Evidence Basis

- **Status:** Field-informed, clean-room reconstruction
- **Evidence basis:** Firsthand qualitative experience using a Microsoft 365 Copilot declarative agent to help the author's team prepare escalations to the author in a previous executive role.
- **Public artifact:** Vendor-neutral instructions, fictional examples, evaluation cases, and dated evaluation records; separate from the private implementation.
- **Public evaluation:** Two recorded first-party Codex-assisted smoke checks from September 2026. They do not evaluate this review's new cross-pattern handoff clarifications.
- **Not established:** Quantified time savings, causal productivity improvement, independent validation, universal applicability, reliable combined-pattern behavior, or safe use without organization-specific controls.

## Origin and Boundary

This pattern is a clean-room reconstruction informed by an internal Microsoft 365 Copilot declarative agent used in a previous executive role. It preserves the organizational lesson without reproducing private instructions, messages, recipient profiles, internal classifications, adoption details, or employer-specific context.

The original internal agent was used in real work. The public instructions in this repository are a separate reconstruction and have only the testing evidence recorded here.

The author describes receiving both requests for decisions and information for awareness. This public specification focuses on preparing a decision or action request; its recorded cases do not establish a general awareness-only workflow. The author, rather than the agent, decided whether to communicate onward.

The public contract's controls are design choices for a reconstruction, not a claim that each rule or readiness label was present or tested in the original agent.

### Origin Story

The related article explains the organizational problem behind this pattern, why the agent was deliberately bounded, and what I learned from using the original implementation:

- [As a CIO, I Used an AI Agent to Prepare Decisions—Not Make Them](https://www.abnerballardo.com/en/post/as-a-cio-i-used-an-ai-agent-to-prepare-decisions-not-make-them/)
- [Como CIO, usé un agente de IA para preparar decisiones—no tomarlas](https://www.abnerballardo.com/es/post/como-cio-use-un-agente-de-ia-para-preparar-decisiones-no-tomarlas/)

## Agent Definition

- **Original implementation:** Microsoft 365 Copilot declarative agent
- **Definitions used:** Declarative agent and agentic workflow
- **Why the definition applies:** The system follows persistent instructions, asks conditional questions, evaluates readiness, stops on missing or unsafe information, and redirects the user when another communication channel is more appropriate.
- **Interaction model:** User-initiated conversation that may continue across targeted clarification turns before producing an output
- **Knowledge and tool access:** The public pattern requires no connected knowledge source or external tool. A private implementation may embed a small registry describing the intended recipient's familiarity with selected projects; it controls explanatory depth but is not a source of project facts.
- **External actions:** None. The public pattern does not send communications, update systems, approve requests, or create commitments.
- **Autonomy boundary:** It may diagnose, question, organize, classify readiness, draft, and recommend another channel. It may not validate source facts, own the sender's recommendation, or make the recipient's decision.
- **Stopping conditions:** Stop or withhold a send-ready draft when decision context is materially incomplete, the source is unsafe, human review is required, or a different channel is more appropriate.
- **Human oversight, handoff, and authority boundaries:** The sender validates the facts and owns the recommendation. The recipient retains the decision. A responsible human selects the channel and approves the final communication.

The public materials are not themselves a deployed agent. They become an agent implementation when configured in a compatible platform or application. Platform-specific implementations belong under [implementations](implementations/) only after they have been publicly built and tested.

## Quick Start

1. Use an AI assistant approved for the information you intend to process.
2. Add [the vendor-neutral agent instructions](agent-instructions.md) as the assistant's behavior or custom instructions.
3. Start with one of the [fictional test examples](examples/) or write your own fictional notes.
4. Ask the assistant to prepare a decision-ready escalation without inventing missing information.
5. Review the result with the [evaluation rubric](evaluations/rubric.md).
6. Adapt the pattern's privacy, channel, and human-review controls before considering live organizational use.

Do not begin by pasting a real email thread. First confirm that the pattern behaves correctly with fictional test inputs and that the selected AI service is approved for the intended data.

## Organizational Problem

Decision-makers often receive one of two unusable escalations:

1. A short message that transfers a problem upward without enough context to decide.
2. A detailed message that forces the recipient to reconstruct the decision from background, technical notes, and unresolved discussion.

Both can delay decisions and obscure accountability. The problem is not simply writing quality; it is the absence of a reliable handoff between the person closest to the issue and the person accountable for the decision.

## Relationship to Other Patterns

[Executive Communication Preparation](../executive-communication-preparation/) addresses a later preparation problem: communicating onward using the leader's direction, maintained recipient guidance, and explicit delegation. This pattern is not restricted to technical audiences, and optional recipient familiarity does not by itself make it the second pattern.

A brief here may give a leader sufficient context to decide or acknowledge the situation. Only the human leader can supply that judgment and direct the onward communication. Completing this brief does not imply that the leader has acted or authorized sending to another recipient.

Use the shared [selection and handoff contract](../../README.md#pattern-selection-and-handoff) and [fictional combined example](../executive-communication-preparation/examples/pattern-handoff.md). Neither pattern requires the other, and the complete combined public workflow has not been behaviorally evaluated.

## Intended Users

- Team leads, technical leaders, product leaders, and operators preparing an escalation
- Executives, founders, and other accountable decision-makers receiving it
- **Accountable responsibilities:** The sender owns factual validation and the recommendation; the recipient owns the decision. A responsible human chooses the channel and approves the final communication.

## When to Use It

- A recipient must decide, approve, reject, align, intervene, or accept a trade-off.
- The sender has raw notes but needs help identifying the actual decision.
- Relevant context is distributed across technical and business details.
- The message needs a clear owner, deadline, recommendation, and next step.

## When Not to Use It

- An urgent or sensitive issue requires a live conversation before a written record.
- Facts are unverified and the consequences of being wrong are material.
- The issue contains personnel, legal, regulatory, security, or confidential details that the selected AI service should not process.
- Multiple stakeholders must negotiate several coupled decisions.
- No meaningful decision, action, risk, or change exists.

## Human Responsibility

The agent may diagnose missing context, organize facts, compare alternatives, expose trade-offs, and draft the brief. It must not:

- invent facts, options, agreement, or urgency;
- select or approve the final decision;
- attribute a recommendation that the sender does not own;
- silently remove material risk or disagreement; or
- decide that sensitive data may be shared.

The sender validates the facts and owns the recommendation. The recipient retains the decision. A responsible human chooses the communication channel and approves the final message.

Readiness describes preparation, not verified truth, decision approval, or authority to send onward. Routine sender review still applies when no additional review is required.

## Required Inputs and Preconditions

The pattern works best when the sender can provide:

- the project code or name when a private recipient-familiarity registry is configured;
- what changed;
- why it matters now;
- the decision or action requested;
- relevant constraints;
- viable options;
- material trade-offs and risks;
- the sender's recommendation;
- the accountable owner; and
- the deadline or next decision point.

Missing information should be identified explicitly. The agent may proceed with low-risk assumptions only when they are visible and do not create a material commitment.

### Optional Recipient Familiarity Configuration

An implementation may maintain a small registry describing how familiar the intended recipient is with selected priority projects. This allows the agent to request and include less established background for projects the recipient follows closely, while requesting more context for projects the recipient knows only generally or does not recognize.

The registry uses:

- **High** for projects whose purpose and established background the recipient already knows well;
- **Medium** for projects the recipient recognizes but may need additional background to interpret; and
- no entry for projects that require the sender to provide full context.

Populate real entries only in an approved private implementation. Record the project code, project name, a short identifying description, and the date the familiarity assessment was reviewed. Do not store live status, incidents, personal information, commercial terms, credentials, or detailed risk records in the registry.

Review entries periodically and downgrade or remove stale ones. If one agent prepares messages for multiple recipients, maintain separate configurations or add an explicit intended-recipient field and test the routing; one person's familiarity must not be applied to another recipient.

## Expected Outcome, Output, or Action

1. **Readiness:** Ready for sender review, needs information, human review required, or use another channel
2. **Decision requested:** One explicit decision or action
3. **Suggested subject:** Topic plus the decision or signal
4. **Executive summary:** What changed and why it matters
5. **Options and trade-offs:** Only viable alternatives
6. **Recommendation:** The sender's preferred path and reasoning
7. **Risks and uncertainty:** Material facts, assumptions, and unknowns
8. **Ownership and timing:** Who acts next and by when
9. **Supporting detail:** A pointer to evidence that should not overload the main brief

## Agent Workflow or Behavior

1. Identify the project and the intended recipient's configured familiarity level, if a private registry is available.
2. Determine what the recipient must understand, decide, or do next.
3. Separate current facts from interpretations, assumptions, and missing information; use recipient familiarity only to calibrate explanatory background.
4. Check whether the issue is suitable for asynchronous written communication.
5. Ask only the minimum targeted questions needed to close blocking gaps.
6. Identify viable options and the material trade-off between them.
7. Confirm that the recommendation belongs to the sender rather than the agent.
8. Draft the shortest brief that preserves decision value.
9. Flag consequential commitments or sensitive uncertainty for human review.
10. Perform a final check for clarity, ownership, timing, and unsupported claims.
11. Hand the brief to the accountable recipient; do not infer a decision or onward instruction from a completed draft.

## Failure Modes

| Failure mode | Required response |
|---|---|
| The requested decision is unclear | Ask a targeted question; do not fabricate an ask. |
| The agent produces an attractive summary without alternatives | Request or identify viable alternatives before marking the brief ready. |
| Compression removes material risk | Restore the risk and explain why it changes the decision. |
| The recommendation is generated rather than owned | Label it as a possible option and require the sender to choose. |
| One message contains several coupled decisions | Split the brief or recommend a meeting. |
| Critical facts are unverified | Mark the output as not ready and identify the required verification. |
| The channel creates unnecessary exposure | Recommend a safer channel or pre-alignment step. |
| Sensitive source material is included | Stop processing and follow the organization's information-handling rules. |

## Privacy and Security Considerations

- Test with synthetic data before introducing organizational content.
- Minimize the information sent to the model and retained in logs.
- Do not paste real email threads merely because they are convenient context.
- Apply organizational rules for confidentiality, personal data, retention, and approved AI services.
- Review combinations of details that could identify people or organizations even after names are removed.
- Keep real recipient-familiarity registries out of the public repository. In private implementations, use minimal approved descriptions, record a review date, and remove obsolete entries.

## Evaluation Criteria

Use the [evaluation rubric](evaluations/rubric.md) and [fictional test cases](evaluations/test-cases.yaml). A useful output should preserve facts and risk while making the requested decision easier to understand.

The [September 11 baseline](evaluations/baseline-2026-09-11.md) records a first-party Codex-assisted smoke check of four cases; its method includes generating or assessing expected responses. The [September 12 baseline](evaluations/baseline-2026-09-12.md) records a six-case follow-up including recipient familiarity. Their runtime/model and scope limitations remain part of the evidence. They are not independent validation, proof of repeated reliability, or tests of this review's handoff and readiness-wording clarifications.

The examples illustrate expected responses; only the dated records describe prior evaluations. The [combined example](../executive-communication-preparation/examples/pattern-handoff.md) illustrates the expected complete workflow; that full sequence remains unevaluated. The second pattern's [dated records](../executive-communication-preparation/evaluations/baseline-2026-10-16-follow-up.md) test its own preparation behavior, including missing leader direction, without evaluating a first-stage agent run.

## Implementation Options

The core behavior is described in [agent-instructions.md](agent-instructions.md). Platform adapters belong under [implementations](implementations/) only after they have been built or tested.

The [Microsoft 365 Copilot implementation guide](implementations/microsoft-365-copilot/) is a field-informed, clean-room reconstruction of the original implementation. It includes dated guidance for configuration, individual use, and incremental organizational rollout.

## Observed Value and Limitations

**Firsthand observation:** The author reports that the private agent helped the team prepare information for the author's judgment and reduced the effort of reconstructing the issue from raw notes. This is qualitative experience, not a measured effect of the public instructions.

**Public evaluation:** The dated first-party smoke checks support only the limited instruction/case observations recorded there. They do not establish model-independent reliability, live adoption, business impact, or behavior of the combined public workflow.

**Design limitation:** The pattern must be adapted for organizational decision rights, risks, communication norms, and approved technology. Its intended contribution is better preparation for human judgment; a completed brief does not establish a good decision or permission to communicate onward.
