# Maintain Executive Communication Guidance

- **Status:** Suggested operating procedure; not tenant-tested. No tenant testing is planned by the author.
- **Owner:** The leader or an explicitly designated guidance owner, distinct from technical agent ownership.

The following procedures apply if an organization adopts this suggestion; they are not an active maintenance or tenant-testing plan for the author.

## Keep Three Records Separate

| Record | Owner and use |
|---|---|
| Current recipient profile | Guidance owner approves work-relevant communication requirements for future cases. |
| Current case evidence | Information owners confirm facts, consequences, uncertainty, ownership, and timing for this case. |
| Per-case direction | Accountable leader supplies decision/acknowledgment, recipient, permitted request, and delegation/review route. |

Use the [canonical profile template](../../recipient-profile-template.md). A profile never supplies current incident facts, authenticates a leader, or grants sending permission. A chat user's suggestion is not an adopted rule; an agent maintainer's ability to edit configuration is not approval of its substantive guidance.

## Private Profile Layout

For the proposed shared agent, maintain separate complete local CEO and regional CIO files. Each includes its recipient identifier, applicable scope, owner, approval/version, review date/trigger, full communication requirements, project familiarity, approved learnings, and a statement of active-guidance completeness.

Use a controlled current location and a separate restricted history/proposals location outside the agent's retrieval scope. Do not connect an entire site containing superseded profiles. A short private version record can identify the effective version without reproducing past correspondence. Every current file must inline all active inherited rules; do not use "same as v1" as an instruction dependency.

Only users authorized to know a profile should receive it or agent access that can surface it. If the two audiences differ, the proposed shared-agent design is not suitable as configured; use separate scopes or an approved common subset. No prompt can substitute for permissions.

## Propose and Adopt a Learning

1. The leader supplies a work-relevant paraphrase of an interaction, distinguishing observation, interpretation, and temporary circumstance. Avoid speculative motives, personal dossiers, or unnecessary organizational politics.
2. In a separate maintenance conversation, ask for existing guidance, the proposed scoped addition/change, its basis/date, question improved, boundaries preserved, and review trigger. A single interaction does not establish a universal preference.
3. The guidance owner accepts, revises, or rejects the proposal outside the agent. Material omissions remain unacceptable even if requested by that owner. Resolve factual disputes with responsible information owners rather than embedding blame in guidance.
4. The owner produces a complete approved next version in private storage. Keep live incident facts and individual delegation out of it. Mark the earlier version superseded in history and remove it from active retrieval scope.
5. Check file permissions and the agent's selected source. If the source reference changes, review the agent configuration and distribute the intended candidate through the platform's update process.
6. Start fresh user sessions and test the changed requirement, unchanged safeguards, and a stale-version attempt before accepting the update. Record actual observed versions and delays. Do not assume an existing conversation forgets previous guidance or that new content is immediately available.

The agent proposes text only. The human owner saves the file and approves the version. This draft does not implement automatic persistence, approval workflows, or synchronization.

## Complete Guidance in Each Session

For each new case/recipient or changed profile, ask for the expected current version and record the version actually available. Have the agent show the available active rules and unresolved references. A named sender or other authorized human compares them with the owner's approved current file through permitted access, including all inherited requirements. Record the confirmer, comparison date, approved source/reference, how guidance was supplied (retrieved or complete text), and confirmed/pending/failed status in preparation notes. Do not invent a ticket or claim independent authentication. A human who supplies and explicitly confirms the complete current text can satisfy this check; the model cannot confirm it for them.

Until the comparison is confirmed, use Needs information and keep any required reviews separately visible. Failed comparison requires corrected complete guidance and a fresh human comparison. Confirmation is neither fact verification, sending permission, nor a waiver of reviews; it is not proof of the model's hidden context. Do not demand it again on an unchanged clarification turn, but repeat it after a material profile/version or recipient/case change.

| Situation | Required response |
|---|---|
| Complete applicable current guidance and confirmed human comparison | Continue checking case evidence and actual delegation. |
| Human comparison pending or failed, including apparently complete retrieval | Needs information; obtain the recorded comparison or corrected full guidance, retaining pending reviews. |
| Excerpt/citation without the full active rules | Obtain a complete owner-confirmed copy through an approved channel; keep missing guidance as a blocker. |
| Inherited rules referenced but absent | Needs information even with complete case facts. |
| Full rules already inlined | Do not demand the superseded file. |
| Wrong, stale, conflicting, inaccessible, or not-yet-ready profile | Resolve with the owner; do not infer preferences or silently use an earlier version. |
| Sensitive text unavailable to this user | Do not bypass access. Stop or route to an authorized preparer. |

Refer to the [build guide's knowledge boundary](build-guide.md#add-and-check-recipient-profiles). Neither retrieval success nor the model's claim of completeness proves that every instruction reached its context. If the team cannot establish effective guidance within the platform, do not approve this configuration for that use.

## Example Maintenance Exercise

Use the [fictional learning example](../../examples/learning-and-guidance-update.md): start with v1, propose a scoped shared-dependency requirement, withhold adoption, then supply a separately approved complete v2. In a fresh team session, check whether the agent asks for current scope evidence and update ownership without treating the profile as proof of wider impact.

Also test a partial v2 referencing absent v1 and a complete inlined v2. The first should block; the second should not demand an old file, but still needs the human comparison. Include pending and failed comparison controls even when the model judges retrieval complete. During tenant acceptance, use fictional files and named test users under [controlled test sharing](build-guide.md#control-test-sharing-and-pilot-access); test-profile adoption does not authorize operational guidance changes. These are hypothetical adoption checks, not tenant observations or planned author work.
