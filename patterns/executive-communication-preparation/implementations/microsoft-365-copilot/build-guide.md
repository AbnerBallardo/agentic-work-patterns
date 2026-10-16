# Suggested M365 Copilot Setup

- **Documentation reviewed:** 2026-10-16.
- **Status:** Suggested setup instructions; not tenant-tested. No tenant testing is planned by the author.

These procedures are for a future adopter who chooses to build this suggestion. They do not describe an active build, testing schedule, or author commitment.

## Before You Build

Name the accountable leader, guidance owner, agent maintainer, and tenant administrator. Confirm licensing, Agent Builder availability, information handling, and permitted sharing with those owners. Use fictional material for all initial checks; this guide does not authorize organizational data use.

Keep the [pattern contract](../../README.md) separate from platform configuration. Do not paste its longer canonical instructions into Agent Builder or move critical safety rules into a document that might not be retrieved.

## Configure the Agent

Microsoft's [current build documentation](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents) describes **New agent → Skip to configure**, followed by the Configure tab. It specifies 30 characters for the name, 1,000 for the description, and 8,000 for instructions. The Model field offers Auto, Quick response, and Think deeper; users can override the default. Skills are a Frontier preview. Optional generation capabilities may be automatically available, so inspect the actual settings rather than assume a blank configuration has none.

The following values are this suggestion's recommendations, not observed tenant settings:

| Field | Proposed value |
|---|---|
| Name | `Executive Communication Prep` |
| Description | `Helps teams prepare executive email using approved recipient guidance and explicit leader direction. Identifies missing evidence and preserves required human review. Does not send or approve.` |
| Instructions | Entire [M365 instruction file](agent-instructions.md), without additions or truncation. Record the saved text and compare it with the source. |
| Default response mode | Think deeper, if available; record the actual mode for each test, including user overrides. This is a proposed choice, not a fixed model identity. |
| Knowledge | Empty for the first chat-supplied fictional-profile smoke check; then add only the selected fictional profile files for retrieval tests. |
| Source prioritization | Enable Only use specified sources if available; retain the factual-evidence rules. |
| Other sources | Disable general web search and people reference where controls are available. Do not add mailbox, Teams history, connectors, or business-app data. |
| Capabilities | No generation capability or action is needed. Turn optional generation features off where supported; record any capability that remains available. No skills. |

Use manual configuration to keep the approved text and scope reviewable. If a conversational builder changes instructions or sources, compare the resulting configuration before proceeding. If the tenant cannot support the intended boundary, document the mismatch and keep the candidate private rather than declaring it equivalent.

## Add and Check Recipient Profiles

Follow [guidance maintenance](guidance-maintenance.md) to create separate complete fictional CEO and CIO profiles from the [template](../../recipient-profile-template.md). Use a supported format such as `.docx` or `.txt`; do not assume repository Markdown is a supported knowledge-file format. Select the specific files, with only current approved versions in retrieval scope.

Microsoft's [knowledge guidance](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-add-knowledge) says SharePoint content uses existing permissions and sensitivity labels; newly added content may remain Preparing before it is used. Embedded uploads expose their information to agent users and have different protections. Only use specified sources prioritizes supplied sources; it does not block general AI knowledge.

For this suggestion, prefer referenced SharePoint files over embedded copies. Test with a normal chat user, not only the owner. A source shown as ready, a citation, or a correct answer to one question is not proof that all active profile rules were supplied. Test missing inherited rules and partial retrieval. Use a complete owner-confirmed text copy in an approved conversation when needed. In every new case/recipient or changed profile, require the [human profile comparison](guidance-maintenance.md#complete-guidance-in-each-session): expected/used version, confirmer/date/source, how guidance was supplied, and confirmed/pending/failed status. Until confirmed, retain Needs information even if the model calls the profile complete. Never repair a retrieval gap by inventing guidance or broadening access.

## Add Starter Prompts

| Name | Prompt |
|---|---|
| Check preparation | `For this fictional case, identify missing evidence, recipient guidance, or applicable leader direction. List blockers and required reviews separately.` |
| Prepare CEO email | `Use the supplied current CEO profile and leader direction to prepare an awareness email. Preserve material facts and uncertainty; do not send.` |
| Prepare CIO email | `Use the supplied current CIO profile and leader direction. Explain relevant local dependencies without inventing facts or approvals.` |
| Propose guidance update | `Help the guidance owner turn this fictional observation into a scoped proposal. Keep it unapproved until human adoption.` |

A starter prompt is not permission or an approval record. A request to prepare an email still needs the actual profile, evidence, direction, and review route.

## Freeze and Check a Private Candidate

1. Record adapter revision/hash, full saved instructions and character count, source file identifiers/versions, active capabilities, date, client, license category, and default/actual response mode in a private configuration record.
2. Use Try it with a new conversation for each fixture. Check a complete direct-send case, a reserved-review case, missing evidence, and a missing-profile case before adding retrieval complexity.
3. Compare the instruction text saved by the platform with the reviewed payload. A successful save is a configuration check, not a behavioral pass.
4. After owner and tenant approval for controlled test sharing, use the created agent with named test users to run the [tenant acceptance cases](rollout-guide.md#tenant-acceptance-cases), including permissions and revocation. Preserve unfavorable responses.
5. Owner-only privacy applies to the initial smoke checks. Controlled test access is permitted during acceptance under the next section; operational pilot access waits until release criteria are met. Any instruction, source, permission, capability, or response-mode change creates a new candidate for affected checks.

There is no tenant result for this suggestion. Do not reuse the pattern's Codex results as evidence that the adapted text or M365 configuration passed.

## Control Test Sharing and Pilot Access

Follow Microsoft's [sharing documentation](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-share-manage-agents) and tenant policy. Chat users interact; owners with Can edit can also manage and share. Groups cannot be owners. Removing agent access does not remove previously granted SharePoint access. Agent updates require Update to become visible; source and agent changes must be checked separately.

Before acceptance, the owner and tenant administrator may approve a documented test plan with named Can chat test users, fictional profiles/cases only, minimum intended source permissions, and a defined test window. Include a designated negative-access user without profile permission. Record who approved the scope and who grants/removes access. This controlled test sharing enables representative-user and revocation checks; it authorizes no operational use, real data, or sending. At closure, remove test agent access and test-source permissions separately; record both outcomes. If tenant policy prevents the test setup, record the blocked checks and withhold pilot acceptance.

After acceptance and separate owner/tenant approval, the operational pilot may have a limited Can chat audience and named individual maintainers, with no organization-wide distribution. Validate the intended audience's access to both profiles before operational use of a combined agent. If profile audiences differ, use separately scoped agents or a common approved guidance set; instructions are not per-profile access controls. Do not grant the team broad profile-edit access to solve a retrieval problem. No sharing or notification is performed by these guides.
