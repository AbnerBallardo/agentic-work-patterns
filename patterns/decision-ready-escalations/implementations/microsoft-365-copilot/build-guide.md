# Build and Configure the Microsoft 365 Copilot Agent

- **Last reviewed:** 2026-09-12
- **Verification boundary:** Current interface details are based on Microsoft documentation and may differ by tenant, license, language, or administrative policy

## Before You Build

Confirm that:

- Agent Builder is enabled in your Microsoft 365 tenant;
- intended users have the licensing required for the configured capabilities;
- your security, privacy, legal, and compliance owners approve the intended data use;
- an accountable owner will maintain and periodically retest the agent; and
- you can begin with synthetic rather than organizational data.

This pattern does not require email, Teams, SharePoint, OneDrive, public-web, or connector knowledge. It also does not require actions. Keeping those features out of the first implementation makes the agent's boundary easier to understand and test.

## Configure the Agent

As of the review date, Microsoft documents this manual path:

1. Open Microsoft 365 Copilot.
2. Select **New agent**.
3. Select **Skip to configure**.
4. Complete the Configure tab.

Use the following configuration:

| Field | Recommended value |
|---|---|
| Name | `Decision-Ready Escalations` |
| Description | `Helps employees clarify an escalation, identify missing decision context, and prepare a concise brief for human review. It does not make or send the decision.` |
| Instructions | Copy the complete [vendor-neutral agent instructions](../../agent-instructions.md), including an approved private recipient-familiarity registry if used. |
| Knowledge | Leave empty for the initial implementation. |
| Capabilities | Leave optional capabilities disabled. |

Using the manual configuration path is intentional. Microsoft's natural-language builder can add knowledge sources or capabilities in response to a description. Before testing, inspect the Configure tab and confirm that the agent has only the configuration you intended.

## Configure the Optional Recipient Familiarity Registry

The registry describes what the intended recipient already knows about selected projects. It helps the agent calibrate how much background to request and include; it does not give the agent factual project knowledge. It is embedded configuration context, not a connected Microsoft 365 knowledge source.

Before copying the instructions into a private agent:

1. Replace the synthetic rows with only the projects for which the intended recipient's familiarity is known.
2. Use project codes where possible to prevent ambiguous matches.
3. Keep each description short: enough to identify the project, but not to represent its status.
4. Assign **High** when the recipient already knows the project well enough that only the current change and decision context are normally necessary.
5. Assign **Medium** when the recipient recognizes the project but still needs background connecting the current issue to its consequences.
6. Add a review date and remove or downgrade stale entries.
7. Confirm that the complete instructions remain within the platform's current configuration limits.

If the agent prepares messages for multiple recipients, do not reuse one person's familiarity labels for everyone. Maintain separate configurations or add an explicit intended-recipient field and test the routing carefully.

Do not add live status, unresolved incidents, personal information, confidential commercial terms, credentials, or detailed risk records to the registry. Those facts must come from approved current input. If the agent requires frequently changing or extensive project knowledge, use an approved knowledge architecture and treat that as a separately governed implementation.

## Add Starter Prompts

Starter prompts should teach the intended behavior rather than imply that the agent can act independently. Suggested prompts:

| Name | Prompt |
|---|---|
| Check readiness | `Help me determine whether this escalation is ready for a decision-maker.` |
| Prepare a brief | `Turn these synthetic notes into a decision-ready escalation. Do not invent missing information.` |
| Find the gaps | `Identify the information that blocks this escalation and ask only the necessary questions.` |
| Choose the channel | `Should this be handled in writing or through a conversation first? Explain the reason.` |

## Test Before Sharing

Use the Agent Builder test experience with the repository's [synthetic test cases](../../evaluations/test-cases.yaml) and score the results with the [evaluation rubric](../../evaluations/rubric.md).

At minimum, confirm that the agent:

- asks for a missing decision instead of inventing one;
- separates facts, assumptions, and unknowns;
- preserves material risks and trade-offs;
- refuses to claim the sender's recommendation;
- recommends another channel when appropriate;
- never claims that it sent, approved, or updated anything; and
- produces consistent results across repeated runs.

Keep the agent private until these behaviors are reliable. Record the model or response mode, test date, configuration version, failures, and changes made after testing.

## Share a Pilot Version

After testing:

1. Create the agent as a private agent first.
2. Add a small pilot group or Microsoft Team with chat-only access.
3. Give edit access only to named maintainers who are accountable for changes.
4. Confirm that tenant policies allow the intended sharing method.
5. Retest after any instruction, knowledge, capability, model, or platform change.

Microsoft currently distinguishes chat users from owners who can edit and manage the agent. Organization-wide discovery and catalog publication may require administrative review. Follow your tenant's current governance rather than assuming that every sharing option is available.

### Use a Microsoft Team as the Access Boundary

The original operating approach used a Microsoft Team for the full IT organization. The Team served two purposes:

1. It created a unified channel for IT communication, examples, questions, and adoption support.
2. Its membership provided a maintainable audience for agent access.

To recreate that approach with the current platform:

1. Create or select a Team whose membership matches the intended agent audience.
2. In the agent's sharing controls, add the Team or its eligible associated group with **Can chat** access.
3. Post the agent's chat link and a short usage explanation in the Team's main channel. If the sharing interface offers a Team notification, verify where it is posted before relying on it.
4. Add individual maintainers—not the group—as owners with **Can edit** access.
5. Test access with representative members, including a recently added member.
6. Test removal and offboarding behavior before treating Team membership as the authoritative access process.

Microsoft Teams uses a Microsoft 365 group to manage standard Team membership, and Agent Builder supports sharing chat access with groups or teams. Exact eligibility and synchronization can depend on the group type, tenant policy, license, and current sharing interface. Validate the mapping in your tenant, especially for guests and private or shared channel membership.

The Team is the operating and discovery channel; sharing access through it does not necessarily mean that the agent executes inside a Teams conversation. Treat in-channel deployment as a separate platform capability that requires its own verification.

## Release Checklist

- [ ] The instructions match the current repository version.
- [ ] No unintended knowledge source or capability is enabled.
- [ ] Recipient-familiarity entries are minimal, approved, current, and tested at each configured level.
- [ ] All synthetic evaluation cases have been run.
- [ ] Unsafe or incomplete inputs produce the expected stopping behavior.
- [ ] Users are told that the agent prepares communication but does not validate facts or make decisions.
- [ ] Data-handling and retention expectations are documented.
- [ ] An owner and review date are assigned.
- [ ] The pilot audience and support channel are defined.
- [ ] Team membership changes have been tested against agent access.

## Platform Notes

Microsoft states that Agent Builder can process prompts, instructions, configurations, output, and Microsoft 365 data through integrated Microsoft 365 and Copilot Studio services. Administrators can restrict availability and sharing. Validate the current product terms, compliance commitments, network requirements, and tenant controls before processing organizational information.

For current interface and governance details, use the [official references](README.md#official-references).
