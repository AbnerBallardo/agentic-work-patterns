# Agentic Work Patterns

> Agents should improve how work is understood, prepared, and carried out without obscuring human responsibility.

This repository contains small, testable patterns for applying AI agents to recurring organizational work. A pattern may support analysis, communication, coordination, creation, operations, decision preparation, or another bounded outcome. The goal is not autonomy for its own sake. Each pattern must define the problem, intended behavior, limits, human responsibility, and evidence needed to evaluate whether it helps.

Decision-Ready Escalations is the first pattern in the collection. It focuses on decision preparation. Executive Communication Preparation is a draft second pattern: it helps a team prepare onward executive communication using maintained leadership guidance and explicit delegation.

## Project Context

For a short introduction to why I am building this collection and how it will evolve, visit the [Agentic Work Patterns construct page](https://www.abnerballardo.com/agentic-work-patterns/).

The story behind the first pattern is available in [English](https://www.abnerballardo.com/en/post/as-a-cio-i-used-an-ai-agent-to-prepare-decisions-not-make-them/) and [Spanish](https://www.abnerballardo.com/es/post/como-cio-use-un-agente-de-ia-para-preparar-decisiones-no-tomarlas/).

## Agent Terminology

There is no single definition of `agent` shared by every platform, research community, or engineering team. This repository uses the term as a broad category and requires each pattern to disclose the behavior and authority of the system it describes.

The following definitions may overlap:

| Form | Meaning |
|---|---|
| Configured assistant | A model specialized through persistent instructions and optional knowledge for a recurring purpose. |
| Declarative agent | A vendor-orchestrated agent configured through instructions, knowledge, capabilities, and optional actions. |
| Agentic workflow | A bounded workflow in which the model applies conditional steps, asks questions, uses stopping rules, or hands control back to a human. |
| Tool-using agent | An agent that selects tools to retrieve information or complete parts of a workflow. |
| Action-taking agent | An agent permitted to create external effects, such as sending a message or updating a record. |
| Autonomous agent | An agent that continues toward a goal across multiple steps with limited human direction. |

These forms are not maturity levels, and a system may fit more than one. Calling a system an agent does not by itself imply tool use, external action, autonomous execution, or decision authority.

Every pattern must identify:

- the definition or definitions being used and why they apply;
- the interaction model;
- available knowledge, tools, and external actions;
- the autonomy and stopping boundaries; and
- the human oversight, handoff, and authority boundaries.

## Pattern Catalog

| Pattern | Status | Purpose |
|---|---|---|
| [Decision-Ready Escalations](patterns/decision-ready-escalations/) | Field-informed, clean-room reconstruction | Turn incomplete or overloaded escalation notes into a concise brief that a human decision-maker can act on. |
| [Executive Communication Preparation](patterns/executive-communication-preparation/) | Draft; field-informed, clean-room reconstruction | Prepare executive communications using leader-maintained recipient guidance, current direction, and explicit review boundaries. |

`Field-informed` means the pattern draws on firsthand operating experience, but the public version is newly written, uses test examples built from fictional information, and does not reproduce a private implementation. It does not imply quantified productivity gains or universal applicability.

In this repository, `synthetic` means fictional information deliberately constructed for testing. It does not reproduce a real email, project, person, or organization; imply statistical representativeness; or guarantee privacy.

## Pattern Selection and Handoff

| Question | Decision-Ready Escalations | Executive Communication Preparation |
|---|---|---|
| What work is being prepared? | A brief for an accountable recipient to decide or act. | An onward executive communication after a leader has supplied direction. |
| What context guides preparation? | Current issue, viable options, recommendation, risks, ownership, and timing; optional recipient familiarity. | Current issue plus maintained recipient guidance, the leader's direction, and explicit delegation/review requirements. |
| Who supplies the consequential judgment? | The recipient makes the decision; the sender owns the recommendation. | The leader supplies direction and delegation; the executive recipient retains any further decision requested. |
| What marks completion? | A brief for human review or a clear explanation of what is missing. | A recipient-specific draft and human handoff within the leader's instruction. |

Both patterns can question incomplete inputs and adapt explanatory depth. Their distinction is the work and human authority they support, not a particular title, level of technical detail, or email format. Each can be used independently.

When used together, the sequence is **team preparation → leader decision or acknowledgment → leader-directed executive preparation → required human review → human sending**. The transition is human-mediated, not an automatic agent-to-agent pipeline.

Carry forward the factual brief, source references and dates, material risks and unknowns, and ownership/timing. Add the leader's actual decision or acknowledgment, onward purpose, intended recipient, permitted commitments, review route, and return conditions, with the direction's issuer, date, source/reference, case scope, and confirmation status. A first-stage readiness label is neither evidence verification nor approval to send onward. Do not carry one recipient's familiarity or access permissions over to another. Return material changes or unresolved direction to the leader.

An awareness-only situation can enter the second pattern after the leader acknowledges it and supplies direction; do not invent a decision request merely to force it through the first pattern. See the [fictional combined example](patterns/executive-communication-preparation/examples/pattern-handoff.md). The complete combined public workflow has not been behaviorally evaluated; the second pattern's dated records cover only its own preparation cases, including missing first-stage leader direction.

## How to Use a Pattern

1. Read the pattern's problem, boundaries, and human-responsibility sections.
2. Adapt the vendor-neutral behavioral contract or agent instructions to your environment.
3. Run the fictional test examples and evaluation cases before using organizational data.
4. Add privacy, security, legal, permission, action, and review controls appropriate to the workflow.
5. Treat the pattern as a starting point, not as evidence that the same design will work unchanged in every organization.

## Repository Principles

- Improve work outcomes without hiding human responsibility.
- Preserve the facts, constraints, uncertainty, provenance, ownership, and consequences necessary for safe and useful work.
- Share reusable operating patterns rather than prompt tricks.
- Keep the core pattern vendor-neutral.
- Use fictional or explicitly cleared examples only.
- State the evidence basis and material limitations of every pattern.

See [Principles](docs/principles.md) for the full set of design constraints and [Pattern Template](docs/pattern-template.md) for the contribution structure.

## Privacy and Safety

Do not submit real emails, customer data, credentials, internal organizational details, or employer- or client-confidential material. Removing names may not be sufficient when context can still identify people or organizations.

See [SECURITY.md](SECURITY.md) before reporting a sensitive issue.

## Contributing

Contributions that improve a pattern, evaluation, or test example are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue or pull request.

## License

Licensed under the [Apache License 2.0](LICENSE).
