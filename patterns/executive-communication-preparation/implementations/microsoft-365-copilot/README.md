# Try the Idea in Microsoft 365 Copilot

**Suggested setup, not tenant-tested. No tenant testing is planned by the author.** Documentation checked October 16, 2026. This is a starting exercise using fictional information.

## Set Up

Microsoft documents **New agent → Skip to configure** in [Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents). Availability depends on your account and tenant settings.

| Field | Suggested value |
|---|---|
| Name | `Executive Communication Prep` |
| Description | `Helps teams prepare executive email from approved recipient guidance and actual leader direction. Asks about gaps; does not decide or send.` |
| Instructions | Copy the entire [M365 instructions](agent-instructions.md). |
| Knowledge | Leave empty for the first exercise; supply the fictional profile in chat. |
| Other features | No web, mailbox, people search, connectors, actions, or preview skills are needed. Inspect defaults and turn optional features off where supported. |

## Try One Case

1. Use the [featured fictional example](../../examples/recipient-specific-preparation.md). Copy its Inputs, not its expected response.
2. Supply the selected profile, case evidence, and leader direction in the conversation. Start a separate conversation for another recipient.
3. Confirm the profile is complete and current. A short statement is enough: who compared it, when, the source/version, and whether it matches. The assistant records this in preparation notes; it cannot confirm it for you.
4. Ask for the email. Check the facts, missing information, scoped ownership, and review route. A fictional direct-send instruction does not authorize an operational message.

The leader chooses whether a real communication needs their review; the sender validates and sends. Only the guidance owner adopts profile changes. See the [profile template](../../recipient-profile-template.md).

## If You Take It Further

A maintained private SharePoint profile is optional. Use only complete approved current guidance and keep old versions outside active retrieval. A citation is not proof all rules were retrieved; missing guidance or human comparison remains a blocker. Microsoft's [knowledge documentation](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-add-knowledge) explains source permissions and the limits of Only use specified sources; it does not block general model knowledge.

For shared experiments, use approved named test users and fictional sources; manage agent and source access separately. Test access is not operational pilot permission. Follow local controls before organizational use; this guide does not supply production readiness.

**Version and limits:** M365 starter 1, 7812 characters; adapted from the [canonical starter instructions](../../agent-instructions.md). This shortened version has not been behaviorally evaluated. The [evidence summary](../../evaluations/README.md) covers earlier Codex instructions, not this setup. A saved configuration or readable draft does not establish reliability or business value.
