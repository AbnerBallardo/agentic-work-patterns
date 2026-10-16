# Pattern Template

Copy this structure into `patterns/<pattern-name>/README.md`. Preserve the shared section names and order. Put pattern-specific configuration under the relevant section as H3 subsections; a common structure does not require identical instructions, examples, or evaluation measures.

```markdown
# Pattern Name

## Status and Evidence Basis

- **Status:** Prototype / Field-informed / Field-tested; identify draft state where applicable.
- **Evidence basis:** Firsthand experience, external evidence, or hypothesis, with limits.
- **Public artifact:** What this repository actually supplies.
- **Public evaluation:** What was run, where results are recorded, and what remains untested.
- **Not established:**

## Origin and Boundary

Separate the original experience from the public reconstruction. Identify proposed safeguards and future extensions without implying they were used or evaluated in the original implementation. Add origin-story links here only when available.

## Agent Definition

- **Definitions used:**
- **Why the definition applies:**
- **Interaction model:**
- **Knowledge and tool access:**
- **External actions:**
- **Autonomy boundary:**
- **Stopping conditions:**
- **Human oversight, handoff, and authority boundaries:**

## Quick Start

Link the instructions, fictional examples, and evaluation rubric. State prerequisites without implying deployment or completed evaluation.

## Organizational Problem

Describe the recurring problem and its consequence.

## Relationship to Other Patterns

Explain overlap, distinct purpose, and any human handoff or dependency. Link shared contracts rather than inventing a required chain. If none applies, say so.

## Intended Users

Name the primary users, affected parties, and accountable owner or operator as applicable.

## When to Use It

-

## When Not to Use It

-

## Human Responsibility

State what the agent may support or perform and what a human must validate, own, approve, monitor, or be able to override.

## Required Inputs and Preconditions

-

## Expected Outcome, Output, or Action

-

## Agent Workflow or Behavior

1.

## Failure Modes

| Failure mode | Required response |
|---|---|
| | |

## Privacy and Security Considerations

-

## Evaluation Criteria

-

## Implementation Options

Link only to implementations that have been built or tested.

## Observed Value and Limitations

Separate firsthand observation, measured results, hypotheses, and unknowns.
```

Each pattern should include a vendor-neutral behavioral specification or agent instructions, at least one synthetic example or scenario, and an evaluation rubric or test case appropriate to the claimed outcome.

## Companion Documentation Conventions

- **Agent instructions:** Use role, operating rules or boundaries, pattern-specific preparation steps, output structure, and a final quality check. Align readiness terms with the README; distinguish routine sender review from additional required approval. Describe handoffs without assuming another agent or a readiness label grants authority.
- **Examples:** Identify all material as fictional and expected, not observed evaluation output. Use `Inputs`, `Expected Response`, and `What to Evaluate` as the common sections; put profiles, leader direction, variants, and multiple recipient drafts under those sections as needed.
- **Evaluation rubric:** Use `Assessment Dimensions`, `Critical Failures`, `Scenario Set`, and `Running and Recording an Evaluation`. Measures may differ by pattern; do not imply numerical scores and qualitative findings are directly comparable. Correct stopping can satisfy a case.
- **Evaluation records:** Preserve dated historical results and their instruction/version coverage. Documentation changes and illustrative responses are not new behavioral runs. Identify uncovered changes instead of silently extending old results.
- **Optional files:** Add a configuration template or structured case file only where useful. Platform implementations are separate from the core documentation and can be deferred.
