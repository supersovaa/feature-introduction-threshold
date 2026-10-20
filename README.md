# Feature Introduction Threshold

A lightweight skill for making the full design cost of a proposed feature visible before adopting it.

## When to use

Use this skill when proposing or deciding whether to include a feature, user operation, mode, or behavior in requirements or design.

## Responsibility

Evaluate the need and benefit of a proposed feature alongside the expected implementation complexity, effects on the wider design, and simpler alternatives.
Prefer the smallest design that satisfies established requirements.
The executable decision rules are in [SKILL.md](SKILL.md).

## Adjacent responsibilities

- [concept-introduction-threshold](https://github.com/supersovaa/concept-introduction-threshold) decides whether named implementation concepts are justified.
- [defense-level](https://github.com/supersovaa/defense-level) defines the required scope of defensive behavior.
- Domain requirements and repository sources of truth determine the behavior that must be supported.

## Installation

Place this repository's `SKILL.md` at `<skills-root>/feature-introduction-threshold/SKILL.md` in the target agent's skill directory, or install the repository through that skill system's repository installation mechanism.
