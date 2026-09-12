# Microsoft 365 Copilot Implementation

- **Last reviewed:** 2026-09-11
- **Platform:** Agent Builder in Microsoft 365 Copilot
- **Implementation type:** Declarative agent applying a bounded agentic workflow
- **Status:** Field-informed, clean-room reconstruction
- **Current verification:** Authoring and sharing steps checked against Microsoft documentation; this public configuration has not been retested in a new tenant

## Purpose

This implementation shows how to configure and introduce the [Decision-Ready Escalations pattern](../../README.md) in Microsoft 365 Copilot. It generalizes the operating approach used in a complex enterprise environment without reproducing a private production configuration, organizational data, or employer-specific controls.

Use Agent Builder for this implementation because the pattern needs persistent instructions and a conversational interface, but no external actions. Copilot Studio may be appropriate if a future version needs more advanced distribution, integrations, or actions. That would be a different implementation and would require new risk controls and testing.

## Configuration Profile

| Element | Configuration |
|---|---|
| Instructions | Use the vendor-neutral [agent instructions](../../agent-instructions.md). |
| Interaction | User initiates a conversation; the agent may ask targeted follow-up questions. |
| Knowledge | No connected organizational knowledge is required. |
| Capabilities | None required. |
| External actions | None. The agent does not send messages or update systems. |
| Distribution | Share chat access with the Microsoft Team or associated group whose membership represents the intended audience. |
| Human control | The sender validates facts, owns the recommendation, chooses the channel, and approves the final communication. |
| Decision authority | The accountable recipient retains the decision. |

## Guides

1. [Build and configure the agent](build-guide.md)
2. [Use the agent to prepare an escalation](user-guide.md)
3. [Pilot and roll out the practice](rollout-guide.md)

## Version Boundary

Microsoft changes product names, interfaces, licensing, available knowledge sources, capabilities, and sharing controls frequently. Treat the date above as part of the guidance. Before implementation, compare these guides with current Microsoft documentation and your tenant's administrative policies.

## Official References

- [Overview of declarative agents for Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/overview-declarative-agent)
- [Build agents with Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents)
- [Best practices for declarative agents](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/declarative-agent-best-practices)
- [Share and manage agents built with Microsoft 365 Copilot](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-share-manage-agents)
- [Agent Builder governance and current limitations](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder)
- [How Microsoft 365 Groups manage Team membership](https://learn.microsoft.com/en-us/microsoftteams/office-365-groups)
