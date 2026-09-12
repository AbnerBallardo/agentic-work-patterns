# Decision-Ready Escalations

## Status and Evidence Basis

- **Status:** Field-informed, clean-room reconstruction
- **Evidence basis:** Firsthand qualitative experience using a Microsoft 365 Copilot declarative agent to improve the preparation of executive communication
- **Not established:** Quantified time savings, causal productivity improvement, universal applicability, or safe use without organization-specific controls

## Origin and Boundary

This pattern is a clean-room reconstruction informed by an internal Microsoft 365 Copilot declarative agent used in a previous executive role. It preserves the organizational lesson without reproducing private instructions, messages, recipient profiles, internal classifications, adoption details, or employer-specific context.

The original internal agent was used in real work. The public instructions in this repository are a separate reconstruction and have only the testing evidence recorded here.

## Agent Definition

- **Original implementation:** Microsoft 365 Copilot declarative agent
- **Public artifact:** Vendor-neutral behavioral specification, synthetic examples, and evaluation material
- **Definitions used:** Declarative agent and agentic workflow
- **Why the definition applies:** The system follows persistent instructions, asks conditional questions, evaluates readiness, stops on missing or unsafe information, and redirects the user when another communication channel is more appropriate.
- **Interaction model:** User-initiated conversation that may continue across targeted clarification turns before producing an output
- **Knowledge and tool access:** The public pattern requires no connected knowledge source or external tool; the user supplies the minimum cleared context required for the escalation.
- **External actions:** None. The public pattern does not send communications, update systems, approve requests, or create commitments.
- **Autonomy boundary:** It may diagnose, question, organize, classify readiness, draft, and recommend another channel. It may not validate source facts, own the sender's recommendation, or make the recipient's decision.
- **Stopping conditions:** Stop or withhold a send-ready draft when decision context is materially incomplete, the source is unsafe, human review is required, or a different channel is more appropriate.
- **Human handoff and decision authority:** The sender validates the facts and owns the recommendation. The recipient retains the decision. A responsible human selects the channel and approves the final communication.

The public materials are not themselves a deployed agent. They become an agent implementation when configured in a compatible platform or application. Platform-specific implementations belong under [implementations](implementations/) only after they have been publicly built and tested.

## Quick Start

1. Use an AI assistant approved for the information you intend to process.
2. Add [the vendor-neutral agent instructions](agent-instructions.md) as the assistant's behavior or custom instructions.
3. Start with one of the [synthetic examples](examples/) or write your own synthetic notes.
4. Ask the assistant to prepare a decision-ready escalation without inventing missing information.
5. Review the result with the [evaluation rubric](evaluations/rubric.md).
6. Adapt the pattern's privacy, channel, and human-review controls before considering live organizational use.

Do not begin by pasting a real email thread. First confirm that the pattern behaves correctly with synthetic inputs and that the selected AI service is approved for the intended data.

## Organizational Problem

Decision-makers often receive one of two unusable escalations:

1. A short message that transfers a problem upward without enough context to decide.
2. A detailed message that forces the recipient to reconstruct the decision from background, technical notes, and unresolved discussion.

Both increase decision latency and weaken accountability. The problem is not simply writing quality; it is the absence of a reliable handoff between the person closest to the issue and the person accountable for the decision.

## Intended Users

- Team leads, technical leaders, product leaders, and operators preparing an escalation
- Executives, founders, and other accountable decision-makers receiving it

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

## Required Inputs

The pattern works best when the sender can provide:

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

## Expected Output

1. **Readiness:** Ready, needs information, human review required, or use another channel
2. **Decision requested:** One explicit decision or action
3. **Suggested subject:** Topic plus the decision or signal
4. **Executive summary:** What changed and why it matters
5. **Options and trade-offs:** Only viable alternatives
6. **Recommendation:** The sender's preferred path and reasoning
7. **Risks and uncertainty:** Material facts, assumptions, and unknowns
8. **Ownership and timing:** Who acts next and by when
9. **Supporting detail:** A pointer to evidence that should not overload the main brief

## Agent Workflow

1. Determine what the recipient must understand, decide, or do next.
2. Separate known facts from interpretations, assumptions, and missing information.
3. Check whether the issue is suitable for asynchronous written communication.
4. Ask only the minimum targeted questions needed to close blocking gaps.
5. Identify viable options and the material trade-off between them.
6. Confirm that the recommendation belongs to the sender rather than the agent.
7. Draft the shortest brief that preserves decision value.
8. Flag consequential commitments or sensitive uncertainty for human review.
9. Perform a final check for clarity, ownership, timing, and unsupported claims.

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

## Evaluation Criteria

Use the [evaluation rubric](evaluations/rubric.md) and [synthetic test cases](evaluations/test-cases.yaml). A useful output must preserve facts and risk while reducing the effort required to understand the decision.

The initial [Codex-assisted manual baseline](evaluations/baseline-2026-09-11.md) records a first-party smoke test of all four synthetic cases. It is not independent validation.

## Implementation Options

The core behavior is described in [agent-instructions.md](agent-instructions.md). Platform adapters belong under [implementations](implementations/) only after they have been built or tested.

The [Microsoft 365 Copilot implementation guide](implementations/microsoft-365-copilot/) is a field-informed, clean-room reconstruction of the original implementation. It includes dated guidance for configuration, individual use, and incremental organizational rollout.

## Observed Value and Limitations

Firsthand qualitative experience indicates that an agent can help people prepare more consistent executive communication and reduce the effort required to reconstruct the decision from raw notes. No controlled measurement, quantified time saving, or independent validation is claimed here.

The pattern must be adapted for the organization's decision rights, risk profile, communication norms, and approved technology. A good brief improves the conditions for judgment; it does not guarantee a good decision.
