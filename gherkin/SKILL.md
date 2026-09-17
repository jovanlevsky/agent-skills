---
name: gherkin
description: Creates gherkin tests for user-proposed feature using information given by user by interviewing them when a user asks to "plan a feature," "plan an implementation," or "write gherkins." Can also be invoked by the planner skill.As
---

# Gherkin Interview

Interview the user before writing Gherkin scenarios.

## Interview Rules

- Ask one focused question at a time.
- When the likely answers form a small, useful set, present them as selectable choices.
- Include a concise description for each choice when the meaning is not obvious.
- Allow free-text input when the user may have an answer outside the listed choices.
- Use `multiSelect` only when more than one answer can be valid.
- Do not ask questions whose answers can be determined from the user's request or the codebase.
- After each answer, use it to narrow the next question rather than repeating it.
- Stop interviewing once the behavior, preconditions, expected outcomes, and important edge cases are clear.

## Suggested Interview Topics

Ask only the topics that are still unknown, adapting the choices to the user's feature:

1. Actor or role performing the behavior.
2. Starting state or preconditions.
3. Main successful outcome.
4. Validation, error, or boundary behavior.
5. Relevant variations or edge cases.

## Gherkin Output

- Write scenarios from the user's behavior and outcomes, not implementation details.
- Use `Feature`, `Scenario`, `Given`, `When`, and `Then` consistently.
- Prefer concrete examples over vague wording.
- Include `And` only when it improves readability.
- Do not invent business rules that the user has not confirmed; ask about them first.
- Write the gherkin tests to an `.md` file.
- Naming convention is as follows:
  - Features: `feat-[name]-gherkins.md`
  - Fixes/bugs: `fix-[bug]-gherkins.md`
- Store in dedicated `/gherkin/` directory at the root of the project. If it doesn't exist, create it.

