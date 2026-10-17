# Decision-Ready Escalations

Help a team bring a human decision-maker enough context to act.

## The Problem

An escalation can be too short to support a decision or so detailed that the recipient must reconstruct the issue. Better wording alone does not supply the missing impact, options, recommendation, owner, or timing.

This pattern is for people preparing a decision or action request and the accountable recipient who receives it.

## The Idea in Practice

In a previous executive role, I used an internal Microsoft 365 Copilot agent to help my team prepare escalations to me. It questioned incomplete notes and helped organize the context before I reviewed it. I retained the decision.

I found this useful for consistency and for reducing repeated reconstruction of an issue. That is qualitative experience, not a measured productivity result. These public instructions are a newly written reconstruction; they do not reproduce the private agent or workplace records.

Read the origin story in [English](https://www.abnerballardo.com/en/post/as-a-cio-i-used-an-ai-agent-to-prepare-decisions-not-make-them/) or [Spanish](https://www.abnerballardo.com/es/post/como-cio-use-un-agente-de-ia-para-preparar-decisiones-no-tomarlas/).

## How It Works

1. The sender provides current notes: what changed, why it matters, the decision requested, viable options, their recommendation, risks, owner, and timing.
2. The assistant identifies missing information, checks whether writing is the right channel, and asks focused questions.
3. It prepares a concise brief that keeps material facts, trade-offs, and uncertainty visible.
4. The sender validates the brief; the recipient decides or acts.

This is a configured conversational assistant. It needs no connected knowledge or external tools and does not send, approve, or update anything. An optional private familiarity list can help it vary background depth for a particular recipient; that list is not project evidence.

If the leader directs onward communication, [Executive Communication Preparation](../executive-communication-preparation/) can help with that next step. The actual human decision and direction must be supplied separately. Neither pattern requires the other; see the [shared handoff](../../README.md#pattern-selection-and-handoff).

## Try It

1. Open the [fictional decision brief](examples/decision-ready-output.md) to see the inputs and expected result.
2. Copy the [agent instructions](agent-instructions.md) into your chosen assistant.
3. Supply only the example's inputs and ask it to prepare the escalation.
4. Check whether the request, options, sender's recommendation, risks, owner, and timing are clear. Remove a key input and see whether it asks instead of guessing.

If you use Microsoft 365 Copilot, follow the [short setup suggestion](implementations/microsoft-365-copilot/README.md). Start with fictional material; no organizational knowledge connection is needed.

## Boundaries and Evidence

The assistant must not invent facts or options, claim the sender's recommendation as its own, conceal material uncertainty, decide, or send. Missing decision context needs clarification. Urgent, sensitive, contested, or consequential issues may need a conversation or additional human review. A readiness label is not approval or factual verification.

**Evidence:** Field-informed reconstruction. The [evidence summary](evaluations/README.md) describes a six-case first-party check of earlier instructions, not independent validation. The current shortened starter has not been behaviorally rerun. The complete two-pattern workflow and business impact are not established.

Optional reading: [other examples](examples/) and the [evidence summary](evaluations/README.md). Full evaluation history remains in Git; it is not a prerequisite for trying the idea.
