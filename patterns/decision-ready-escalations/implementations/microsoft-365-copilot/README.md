# Try the Idea in Microsoft 365 Copilot

**Suggested setup; this shortened public configuration has not been tenant-tested.** The original private practice used M365 Copilot, but that does not validate these public instructions. Documentation checked October 16, 2026. No tenant testing is planned by the author.

## Set Up

Microsoft documents **New agent → Skip to configure** in [Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents). Availability depends on your account and tenant settings.

| Field | Suggested value |
|---|---|
| Name | `Decision-Ready Escalations` |
| Description | `Helps a sender prepare a concise decision brief, identify missing context, and preserve human review. Does not decide or send.` |
| Instructions | Copy the complete [starter instructions](../../agent-instructions.md). |
| Knowledge | Leave empty; use fictional notes supplied in the conversation. |
| Other features | No web, mailbox, connectors, or actions are needed. Inspect defaults and disable optional features where supported. |

## Try One Case

1. Copy the Inputs from the [fictional decision brief](../../examples/decision-ready-output.md), leaving out the expected response.
2. Ask the assistant to prepare an escalation. Answer any material questions using only the fictional facts.
3. Check that the decision requested, options, sender's recommendation, risks, owner, and deadline are visible. The human recipient still decides.
4. Remove an important input and see whether the assistant asks instead of inventing an answer.

No project familiarity list is needed for the first exercise. If useful later, supply only a recipient's approved project familiarity and review date; use it for background depth, not current facts.

## Limits

Start with fictional information and review outputs yourself. The assistant does not independently verify evidence, approve, or send. Urgent, sensitive, contested, or consequential issues may need a different channel or further human review.

For a shared experiment, use approved named test users and fictional data. Agent access and source access are separate; a trial does not authorize operational use. Local permissions and controls remain the adopter's responsibility.

**Version:** The current starter instructions are 4680 characters. They have not been behaviorally rerun. The [evidence summary](../../evaluations/README.md) covers earlier instructions; it does not establish this M365 setup's reliability or productivity. No tenant-testing project is required to share or explore the suggestion.
