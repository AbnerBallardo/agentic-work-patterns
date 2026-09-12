# Agentic Work Patterns

> Agents should not replace executive judgment. They should prepare decisions for human judgment.

This repository contains small, testable patterns for using AI agents to improve decisions, coordination, and everyday organizational work. The goal is not autonomy for its own sake. Each pattern should make a recurring problem easier to understand, improve the quality of the work handed from one person to another, and keep consequential judgment with an accountable human.

## Pattern Catalog

| Pattern | Status | Purpose |
|---|---|---|
| [Decision-Ready Escalations](patterns/decision-ready-escalations/) | Field-informed, clean-room reconstruction | Turn incomplete or overloaded escalation notes into a concise brief that a human decision-maker can act on. |

`Field-informed` means the pattern draws on firsthand operating experience, but the public version is newly written, uses synthetic examples, and does not reproduce a private implementation. It does not imply quantified productivity gains or universal applicability.

## How to Use a Pattern

1. Read the pattern's problem, boundaries, and human-responsibility sections.
2. Adapt the vendor-neutral agent instructions to your environment.
3. Run the synthetic examples and evaluation cases before using organizational data.
4. Add privacy, security, legal, and review controls appropriate to the consequences of the workflow.
5. Treat the pattern as a starting point, not as evidence that the same design will work unchanged in every organization.

## Repository Principles

- Improve human judgment; do not hide or replace human accountability.
- Preserve facts, uncertainty, options, trade-offs, ownership, and timing.
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
