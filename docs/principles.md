# Principles

## 1. Improve Work; Preserve Responsibility

An agent may analyze, organize, create, retrieve, coordinate, recommend, or perform bounded actions. Its role must be explicit, and human responsibility must remain visible wherever the consequences require human ownership or judgment.

## 2. Start With the Work Problem

Use an agent because a recurring work problem needs improvement—not because a model capability is available. Define the user, intended outcome, operating context, and failure cost before choosing an implementation.

## 3. Preserve Work Value

An agent that transforms, summarizes, generates, or acts on information must preserve what makes the work correct and useful, including as applicable:

- relevant facts and source provenance;
- requirements, constraints, and success criteria;
- material risks, uncertainty, and disagreement;
- ownership, permissions, and timing; and
- information needed to review, reverse, or continue the work safely.

Remove or compress detail only when doing so does not damage the intended outcome, evidence, safety, or accountability.

## 4. Make Assumptions Visible

Agents must not manufacture missing context, evidence, completion, or authority. They should ask for blocking information, stop, or continue with clearly labeled assumptions when the consequences allow it.

## 5. Bound Authority and Autonomy

Every pattern must state what the agent may access, decide, generate, change, or communicate. Define tool and data access, external effects, stopping conditions, escalation paths, and the person or system authorized to approve or reverse consequential actions.

## 6. Keep Humans in Consequential Loops

Human review is required when an output or action could create material commitments, change accountability, accept risk, affect people, or create legal, regulatory, financial, security, safety, or reputational consequences.

## 7. Use the Safest Appropriate Workflow

An available agent output or action is not automatically the right next step. Sensitive, ambiguous, urgent, contested, or high-impact work may require human interaction, specialist review, an approved system, or a different workflow.

## 8. Separate the Pattern From the Platform

The core pattern defines the organizational problem and behavioral contract. Product-specific configuration belongs in an implementation adapter and should not become the source of truth.

## 9. State Evidence and Limits

Every pattern should say whether it is a prototype, a field-informed reconstruction, or supported by repeated observation. Qualitative experience is useful evidence, but it should not be presented as quantified or independently validated performance.

## 10. Protect Source Boundaries

Use synthetic examples by default. Do not publish private instructions, messages, internal classifications, stakeholder profiles, or operational records. Generalize the durable behavior and disclose only what is necessary for others to understand and evaluate it.

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

When describing a pattern, briefly state what the assistant does, what it can access or change, when it stops, and who remains responsible. A production implementation or tenant evaluation is not required to share a clearly labeled starting point.
