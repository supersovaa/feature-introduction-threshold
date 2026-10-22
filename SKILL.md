---
name: feature-introduction-threshold
description: Evaluate whether to introduce, retain, simplify, or remove a feature, user operation, mode, or behavior in requirements or design by comparing its current value, continuing costs, and simpler alternatives.
---

# Feature Introduction Threshold

Use this skill when deciding whether to introduce, retain, simplify, or remove a feature, user operation, mode, or behavior in requirements or design.

This skill targets a single-user AI-agent design workflow.

## Core rule

Choose the simplest functional scope that satisfies current user decisions and established requirements.
Make both the benefit and the continuing cost of a functional choice visible, whether the behavior is proposed or already implemented.

Treat recovery, retries, fallback paths, migration, legacy-format support, and backward compatibility as functional choices whenever their guarantees are proposed or reconsidered.

## Evaluate the functional choice

For the behavior under consideration:

1. Identify the concrete user goal, current requirement, actual use, and expected benefit. Distinguish required guarantees from optional behavior.
2. Compare introducing or retaining the behavior with simplifying or removing it. Consider the simplest viable alternative, such as reporting a failure, rejecting unsupported older inputs, using a corresponding historical version, or omitting an optional path.
3. Compare the benefit with the whole-workflow cost: implementation and integration, additional code and states or branches, tests, future design changes, ongoing reviews, and other continuing maintenance. Include one-time removal or transition work when material.
4. Explain consequential uncertainty proportionately, using qualitative comparisons where precise estimates lack evidence.

Evaluate the affected workflow rather than only an isolated control or code change.
Treat existing code, design text, and tests as evidence of present behavior and costs; base the case for continued support on current requirements and ongoing value.

## Decide the functional scope

Use explicit user decisions and current requirements as the target. When a newer user decision removes or narrows a behavior, revise the relevant requirements and design to that target, including when an earlier design specified the behavior.

Recommend introduction or retention when the benefit and required guarantees justify their continuing costs. Prefer simplification or removal when the user's goal can be met more economically by a smaller design.
Present optional additions and consequential changes to still-required guarantees for user decision before adopting them.

For settled changes to already implemented behavior, use `implemented-feature-change-handoff` to carry the required implementation and test changes into planning.

## Responsibility boundary

This skill owns the value and scope decision for introducing, retaining, simplifying, or removing functionality in requirements and design.
`implemented-feature-change-handoff` owns transferring settled changes to implementation and test planning.
`concept-introduction-threshold` owns the justification for named implementation concepts.
`defense-level` owns the required defensive scope.
Domain requirements and repository sources of truth provide the current contractual and domain constraints.
