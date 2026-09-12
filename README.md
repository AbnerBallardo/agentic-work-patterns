# Agentic Work Patterns

> Agents should improve how work is understood, prepared, and carried out without obscuring human responsibility.

This repository contains small, testable patterns for applying AI agents to recurring organizational work. A pattern may support analysis, communication, coordination, creation, operations, decision preparation, or another bounded outcome. The goal is not autonomy for its own sake. Each pattern must define the problem, intended behavior, limits, human responsibility, and evidence needed to evaluate whether it helps.

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

`Field-informed` means the pattern draws on firsthand operating experience, but the public version is newly written, uses synthetic examples, and does not reproduce a private implementation. It does not imply quantified productivity gains or universal applicability.

## How to Use a Pattern

1. Read the pattern's problem, boundaries, and human-responsibility sections.
2. Adapt the vendor-neutral behavioral contract or agent instructions to your environment.
3. Run the synthetic examples and evaluation cases before using organizational data.
4. Add privacy, security, legal, permission, action, and review controls appropriate to the workflow.
5. Treat the pattern as a starting point, not as evidence that the same design will work unchanged in every organization.

## Repository Principles

- Improve work outcomes without hiding human responsibility.
- Preserve the facts, constraints, uncertainty, provenance, ownership, and consequences necessary for safe and useful work.
- Share reusable operating patterns rather than prompt tricks.
- Keep the core pattern vendor-neutral.
- Use synthetic or explicitly cleared examples only.
- State the evidence basis and material limitations of every pattern.

See [Principles](docs/principles.md) for the full set of design constraints and [Pattern Template](docs/pattern-template.md) for the contribution structure.

## Privacy and Safety

Do not submit real emails, customer data, credentials, internal organizational details, or employer- or client-confidential material. Removing names may not be sufficient when context can still identify people or organizations.

See [SECURITY.md](SECURITY.md) before reporting a sensitive issue.

## Contributing

Contributions that improve a pattern, evaluation, or synthetic example are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening an issue or pull request.

## License

Licensed under the [Apache License 2.0](LICENSE).
