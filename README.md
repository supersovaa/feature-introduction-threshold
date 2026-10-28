# Feature Introduction Threshold

A lightweight skill for choosing the smallest useful functional scope, including whether an optional feature is worth proposing.

This skill targets a single-user AI-agent design workflow.

## When to use

Use this skill when defining or revising functional scope in requirements or design, including proposals to introduce, retain, simplify, or remove a feature, user operation, mode, or behavior.

## Responsibility

Screen optional functional proposals for concrete current value before raising them, accounting for the user's attention and decisions alongside implementation and ongoing maintenance.
Choose the smallest viable scope for proposed or existing behavior, including recovery, retries, fallbacks, migrations, legacy-format support, and backward compatibility.
Existing code, design, and tests describe the current state; current requirements and user decisions determine the target.

The executable decision rules are in [SKILL.md](SKILL.md).

## Adjacent responsibilities

- [implemented-feature-change-handoff](https://github.com/supersovaa/implemented-feature-change-handoff) transfers settled changes to implemented functionality into implementation and test planning.
- [concept-introduction-threshold](https://github.com/supersovaa/concept-introduction-threshold) decides whether named implementation concepts are justified.
- [defense-level](https://github.com/supersovaa/defense-level) defines the required scope of defensive behavior.
- Domain requirements and repository sources of truth provide the current contractual and domain constraints.

## Installation

Place this repository's `SKILL.md` at `<skills-root>/feature-introduction-threshold/SKILL.md` in the target agent's skill directory, or install the repository through that skill system's repository installation mechanism.
