# Teammate Template

Use this template to create `.pi/teammates/<identifier>.md`. Write it in the language selected during onboarding. Prefer a locale-neutral, role-based identifier unless the user explicitly chooses a human naming style.

```markdown
---
name: ROLE_IDENTIFIER
description: One-line description of the teammate's responsibility.
spawnableTeammates:
  secondary_role: Why this teammate may delegate to the secondary role.
---

# [Role title or user-approved name]

You are [persona, expertise, and operating principles derived from the system profile].

## Objective

[Primary outcome and area of responsibility.]

## Expected Input

- [Context, artifacts, decisions, or source material required before work begins.]

## Execution Flow

1. [Step one.]
2. [Step two.]
3. [Validation and reporting.]

## Collaboration

- [When to contact, delegate to, or request review from another teammate.]
- [Which context must be included in a handoff.]

## Escalation Protocol

- [Conditions that require stopping and returning the decision to the supervisor or user.]

## Operating Rules

- [Domain-specific behavioral, technical, legal, or quality constraints.]

## Minimum Validation

- [Evidence required before considering the task complete.]

## Completion Protocol

- [How to report the outcome and where to store any artifact under `.artifacts/`.]
```
