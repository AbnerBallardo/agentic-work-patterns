# Example: Excessive Detail

This example uses fictional information and does not reproduce a real organizational situation.

## Raw Input

> We started planning the customer portal migration several months ago. The team has held recurring technical sessions and reviewed application logs, deployment scripts, browser compatibility, several unresolved interface defects, and a long history of environment differences. A supplier has explained that one dependency will take another week. Engineering discussed rebuilding part of the integration, adding temporary manual processing, launching only part of the portal, or moving the date. Several people have different views. Leadership needs an update.

## Agent Diagnosis

The note contains useful background, but it does not yet identify:

- whether leadership is only being informed or must make a decision;
- the customer or business consequence;
- which options remain viable;
- the team's recommendation;
- the accountable owner; or
- the decision deadline.

## Appropriate Agent Response

```text
Readiness:
Needs information

Decision requested:
Confirm whether leadership must approve a launch-date change, accept a reduced scope, or only receive an update.

Information to preserve:
- The external dependency changes the planned timing.
- The team has identified partial launch, temporary manual processing, and date movement as possible responses.

Information to move out of the main brief:
- Meeting history, log-review detail, deployment-script detail, and the full defect chronology unless they change the decision.

Blocking questions:
1. What customer or business outcome is at risk?
2. Which options are genuinely viable, and what is the primary trade-off of each?
3. What does the accountable team recommend, who owns execution, and when is the decision needed?
```
