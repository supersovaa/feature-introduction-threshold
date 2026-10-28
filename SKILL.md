---
name: feature-introduction-threshold
description: Define or revise functional scope in requirements or design, screening proposals to introduce, retain, simplify, or remove a feature, operation, mode, or behavior for current value, user decision burden, and ongoing costs.
---

# Feature Introduction Threshold

Use this skill when defining or revising functional scope in requirements or design, including proposals to introduce, retain, simplify, or remove a feature, user operation, mode, or behavior.

This skill targets a single-user AI-agent design workflow.

## Core rule

Choose the simplest functional scope that satisfies current user decisions and established requirements.
Evaluate assistant-originated optional behavior before proposing it, including the attention and decision effort that presenting the option would require of the user.

Treat recovery, retries, fallback paths, migration, legacy-format support, and backward compatibility as functional choices whenever their guarantees are proposed or reconsidered.

## Evaluate the functional choice

For the behavior under consideration:

1. Identify the concrete user goal, current requirement, actual use, and expected benefit. Distinguish required guarantees from optional behavior.
2. Compare introducing or retaining the behavior with simplifying or removing it. Consider the simplest viable alternative, such as reporting a failure, rejecting unsupported older inputs, using a corresponding historical version, or omitting an optional path.
3. Compare the benefit with the whole-workflow cost: user attention, decision effort, and understanding of added contracts; implementation and integration, additional code and states or branches, tests, future design changes, ongoing reviews, and other continuing maintenance. Include one-time removal or transition work when material.
4. Explain consequential uncertainty proportionately, using qualitative comparisons where precise estimates lack evidence.

Evaluate the affected workflow rather than only an isolated control or code change.
Treat existing code, design text, and tests as evidence of present behavior and costs; base the case for continued support on current requirements and ongoing value.

## Decide the functional scope

Use explicit user decisions and current requirements as the target. When a newer user decision removes or narrows a behavior, revise the relevant requirements and design to that target, including when an earlier design specified the behavior.

Recommend introduction or retention when its concrete current benefit justifies its whole-workflow cost. Prefer simplification or removal when the user's goal can be met more economically by a smaller design.
Raise an assistant-originated optional proposal only when its current benefit also justifies the user's effort to consider it. Keep the contract limited to established requirements and user-decided options, and seek a user decision before changing a still-required guarantee.

For settled changes to already implemented behavior, use `implemented-feature-change-handoff` to carry the required implementation and test changes into planning.

## Responsibility boundary

This skill owns the value and scope decision for proposing, introducing, retaining, simplifying, or removing functionality in requirements and design.
`implemented-feature-change-handoff` owns transferring settled changes to implementation and test planning.
`concept-introduction-threshold` owns the justification for named implementation concepts.
`defense-level` owns the required defensive scope.
Domain requirements and repository sources of truth provide the current contractual and domain constraints.
