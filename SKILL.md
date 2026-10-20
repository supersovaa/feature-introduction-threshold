---
name: feature-introduction-threshold
description: Evaluate proposed features, user operations, modes, or behaviors during requirements or design by showing their benefits, implementation complexity, design-wide effects, and simpler alternatives before deciding whether to include them.
---

# Feature Introduction Threshold

Use this skill when proposing or deciding whether to include a feature, user operation, mode, or behavior in requirements or design.

This skill targets a single-user AI-agent design workflow.

## Core rule

Make the incremental complexity of a proposed feature visible before recommending its inclusion.
Prefer the simplest design that meets established requirements.

## Evaluate the proposal

When evaluating a proposed feature:

1. State the concrete need and expected benefit.
2. Outline the implementation approach and its qualitative complexity relative to the simplest viable baseline.
3. Identify meaningful downstream effects, such as additional states, transitions, failure handling, persistence, interactions with other features, and tests. Describe the effects actually relevant to the proposal.
4. Compare with a simpler alternative, including omitting the feature from the initial design when viable.
5. Make consequential uncertainty explicit instead of implying a precise estimate.

Evaluate the whole affected workflow, not just the visible control or isolated code change.
Keep the explanation proportional to the proposal; numerical scores, exact time estimates, and additional process are unnecessary.

## Decide inclusion

Use established requirements and explicit user decisions as constraints.
Recommend optional features when their value warrants the added complexity, and otherwise favor the simpler design.
Present optional additions for user decision rather than treating a suggestion as an accepted requirement.
For an explicitly requested feature with significant design effects, explain those effects and any simpler alternatives that still satisfy the requirement.

## Responsibility boundary

This skill owns evaluating proposed functionality for inclusion and explaining its design-wide complexity during requirements and design.
`concept-introduction-threshold` owns whether named implementation concepts are justified.
`defense-level` owns the required scope of defensive behavior.
Domain requirements and repository sources of truth own the behavior the design must satisfy.
