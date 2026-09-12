# Build and Configure the Microsoft 365 Copilot Agent

- **Last reviewed:** 2026-09-11
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
| Instructions | Copy the complete [vendor-neutral agent instructions](../../agent-instructions.md). |
| Knowledge | Leave empty for the initial implementation. |
| Capabilities | Leave optional capabilities disabled. |

Using the manual configuration path is intentional. Microsoft's natural-language builder can add knowledge sources or capabilities in response to a description. Before testing, inspect the Configure tab and confirm that the agent has only the configuration you intended.

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
