---
name: requirement-clarification
description: Clarify a software requirement before domain modeling or implementation. Use to extract goals, actors, scope, business rules, ambiguities, constraints, risks, and candidate acceptance criteria from natural-language requirements and repository evidence.
allowed-tools: Read Grep Glob
---

# Requirement Clarification

## Inputs

- Raw requirement or issue description
- Existing requirement documents when available
- Relevant repository code, tests, interfaces, and configuration
- Existing domain glossary and architecture decisions when available

## Procedure

1. Restate the intended business outcome without adding implementation details.
2. Identify actors, triggers, preconditions, inputs, outputs, and observable results.
3. Separate included scope, excluded scope, assumptions, constraints, and dependencies.
4. Extract explicit business rules.
5. Search existing code and tests for current behavior that affects the requirement.
6. Identify contradictions, undefined terms, missing boundaries, and unverifiable language.
7. Generate candidate acceptance criteria using observable behavior.
8. Create an ambiguity backlog instead of silently deciding unclear business rules.
9. Recommend whether the requirement can proceed to domain modeling or requires human review.

## Ambiguity classification

Classify each unresolved item as one of:

- business-goal
- business-rule
- scope
- terminology
- behavior-priority
- non-functional-requirement
- architecture-constraint
- external-dependency
- verification-gap

## Output quality rules

- Distinguish facts, assumptions, inferences, and decisions.
- Cite repository files when inferring existing behavior.
- Avoid architecture and technology selection.
- Avoid vague acceptance language such as “works well”, “fast”, or “user friendly”.
- Do not mark an unresolved requirement as ready for autonomous execution.

## Required output sections

1. Goal and business value
2. Actors and systems
3. Scope
4. Business rules
5. Candidate acceptance criteria
6. Assumptions and constraints
7. Ambiguity backlog
8. Repository evidence
9. Risks
10. Readiness recommendation

## Readiness recommendation

Use exactly one of:

- `READY_FOR_DOMAIN_MODELING`
- `HUMAN_REVIEW_REQUIRED`
- `INSUFFICIENT_EVIDENCE`
