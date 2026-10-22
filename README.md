# Feature Introduction Threshold

A lightweight skill for deciding whether functional behavior earns its initial and continuing complexity.

This skill targets a single-user AI-agent design workflow.

## When to use

Use this skill when deciding whether to introduce, retain, simplify, or remove a feature, user operation, mode, or behavior in requirements or design.

## Responsibility

Compare current user goals and benefits with whole-workflow implementation and continuing maintenance costs, then choose the simplest viable scope.
This applies to proposed and already implemented behavior, including recovery, retries, fallbacks, migrations, legacy-format support, and backward compatibility.
Existing code, design, and tests describe the current state; current requirements and user decisions determine the target.

The executable decision rules are in [SKILL.md](SKILL.md).

## Adjacent responsibilities

- [implemented-feature-change-handoff](https://github.com/supersovaa/implemented-feature-change-handoff) transfers settled changes to implemented functionality into implementation and test planning.
- [concept-introduction-threshold](https://github.com/supersovaa/concept-introduction-threshold) decides whether named implementation concepts are justified.
- [defense-level](https://github.com/supersovaa/defense-level) defines the required scope of defensive behavior.
- Domain requirements and repository sources of truth provide the current contractual and domain constraints.

## Installation

Place this repository's `SKILL.md` at `<skills-root>/feature-introduction-threshold/SKILL.md` in the target agent's skill directory, or install the repository through that skill system's repository installation mechanism.
