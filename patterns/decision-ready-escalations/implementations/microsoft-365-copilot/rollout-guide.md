# Pilot and Roll Out the Practice

- **Last reviewed:** 2026-09-11
- **Audience:** Leaders, agent owners, change leads, and governance partners
- **Approach:** Incremental adoption rather than a mandatory big-bang release

## Treat This as a Management Practice

The value does not come only from installing an agent. It comes from teaching people to clarify the decision, test their recommendation, expose uncertainty, and choose the appropriate channel before escalating.

In prior field use, people were often surprised that the agent improved more than email structure. Its questions helped them understand the problem and become clearer about the message they wanted to deliver. That makes the implementation partly a communication-coaching system—an ability that is otherwise difficult to teach consistently across a large organization.

This is qualitative, firsthand experience. It is not a quantified productivity claim.

## Use the Team as the Operating Home

In the original implementation, one Microsoft Team represented the IT organization. Sharing the agent with that Team solved two connected problems: it established a unified channel for IT and provided a practical way to manage who could access the agent.

This design makes adoption part of an existing operating environment rather than a separate technology launch. Use the Team to:

- publish the agent link and concise usage guidance;
- share synthetic or explicitly cleared examples;
- explain what the agent can and cannot do;
- collect questions, failures, and improvement requests;
- announce instruction or platform changes; and
- give new members a consistent entry point.

Treat Team membership as an access-control dependency. Define who approves membership, how departures are handled, whether guests are allowed, and how access is verified after membership changes. Keep agent ownership assigned to named individuals so maintenance responsibility does not disappear inside the group.

## Rollout Stages

| Stage | Scope | What to learn | Exit condition |
|---|---|---|---|
| 1. Owner validation | Agent owner using synthetic cases | Whether instructions and stopping rules behave correctly | Critical evaluation cases pass consistently |
| 2. Small pilot | Trusted users with varied roles | Where people misunderstand the agent or the escalation format | Common failure modes and coaching needs are documented |
| 3. Team practice | Selected teams and leaders | Whether the practice improves preparation without blocking urgent access | Leaders apply the norm consistently and exceptions work |
| 4. Controlled expansion | Additional teams approved by governance | Whether the pattern transfers across contexts | Ownership, support, measurement, and periodic review are sustainable |

Do not expand only because adoption is high. Expand when the outputs are safer and more useful, the boundaries are understood, and someone can maintain the implementation.

## Introduce the Norm in Daily Work

Leaders should model the practice before requiring it from others. Use the agent on your own drafts, show examples with synthetic or cleared content, and explain which questions changed your thinking.

For routine hallway, chat, or meeting interruptions, a leader can say:

> Before we work through this, have you tested the framing with the agent? If not, use it first, then come back or send me the brief.

For urgent situations:

> Let's handle this now. Next time, if circumstances allow, use the agent first so we can reach the decision faster.

Apply the norm with judgment. People are learning a new behavior, and urgency, sensitivity, access needs, or power dynamics may make immediate human attention more appropriate.

## Coach the Thinking, Not Just the Format

When reviewing an output, discuss:

- whether the decision is explicit;
- which facts remain uncertain;
- why the listed options are genuinely viable;
- who owns the recommendation;
- what risk could change the decision;
- whether the recipient has the authority to act; and
- whether written communication is the right channel.

Avoid turning the template into a bureaucratic form. A short escalation with one clear decision may need only a few lines. The structure exists to reduce reconstruction effort, not to reward completeness for its own sake.

## Governance and Ownership

Assign responsibility for:

| Responsibility | Suggested owner |
|---|---|
| Agent instructions and versioning | Business owner with an agent maintainer |
| Data and acceptable-use controls | Security, privacy, legal, and compliance owners as applicable |
| Sharing and tenant administration | Microsoft 365 administrator |
| Team membership and access lifecycle | Team owners with identity or access administrators |
| Evaluation and regression testing | Agent owner with representative users |
| Communication coaching | People leaders and enablement partners |
| Incident and feedback intake | Named support owner |

Do not use the agent's prose quality as a proxy for employee performance. Do not penalize someone for bypassing it when urgency, sensitivity, accessibility, or responsible judgment requires another route.

## Measure Without Overclaiming

Useful pilot evidence may include:

- recurring missing inputs identified by the agent;
- proportion of synthetic or cleared test cases meeting the rubric;
- number and type of clarification turns;
- user-reported changes in problem understanding;
- leader-reported reduction in decision reconstruction effort;
- inappropriate-channel recommendations caught before sending; and
- failures, unsafe behavior, and exception cases.

Separate observed behavior from inferred business impact. Do not convert subjective feedback into claims of time savings, productivity, or decision quality without an appropriate measurement design.

## Review Triggers

Recheck the implementation:

- on a scheduled cadence appropriate to your organization;
- after changes to Microsoft 365 Copilot, Agent Builder, models, or licensing;
- after modifying instructions, knowledge, capabilities, or sharing;
- when the agent begins producing materially different results;
- after a policy, data-handling, or organizational change; and
- before expanding to a new team or use case.

Record the review date and configuration version. Re-run the [synthetic evaluations](../../evaluations/test-cases.yaml) rather than assuming that prior behavior still holds.
