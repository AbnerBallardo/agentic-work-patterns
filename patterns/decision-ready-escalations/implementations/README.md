# Implementations

This directory is reserved for platform-specific adapters that have actually been built or tested.

## Available Implementations

| Platform | Status | Last reviewed |
|---|---|---|
| [Microsoft 365 Copilot](microsoft-365-copilot/) | Field-informed, clean-room reconstruction; current authoring flow checked against Microsoft documentation | 2026-09-11 |

An implementation should:

- reference the vendor-neutral [pattern](../README.md) and [agent instructions](../agent-instructions.md);
- document the tested platform and relevant configuration assumptions;
- state what data the platform stores, transmits, or logs;
- explain required human-review controls;
- include synthetic setup and evaluation examples; and
- identify observed behavior and unresolved limitations.

Do not add empty platform directories or copy a private production configuration into this public repository.
