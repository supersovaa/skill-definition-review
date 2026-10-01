---
name: skill-definition-review
description: Review skill definitions as complete behavioral specifications, checking frontmatter, activation scope, rule consistency, responsibility boundaries, and whether the whole skill expresses its intended behavior with a minimal rule set.
---

# Skill Definition Review

Use this skill when reviewing a `SKILL.md` file or an equivalent skill definition.

Treat the changed skill as one complete behavioral specification.
Use the diff to understand the intended change, then judge the resulting full definition.

## Check activation

Review the frontmatter description together with the opening usage guidance.
Confirm that they express the skill's purpose, applicable situations, and important distinctions introduced by the body.

## Check the rule system

Read all rules together before reporting findings.
Check the applicability of each rule, especially distinctions between different modes or states of work.
When a skill can govern both ordinary work and review, determine whether the same rules cover both contexts.
When review needs distinct behavior, place that behavior in a review-specific companion skill and treat an implicit or ambiguous review path as a coverage gap.
Check for duplicated behavior, conflicting instructions, uncovered cases, and broad rules that override narrower intended behavior.

## Check responsibility boundaries

Confirm that the skill governs one coherent concern.
Keep surrounding workflow, repository, implementation, and process details with their respective skills unless the core behavior depends on them.
Prefer the smallest rule set that preserves the intended behavior.

## Check the change across the whole skill

Identify the intended behavioral change from the request or review context.
Trace that change through the frontmatter, usage guidance, relevant rules, and closing responsibility statement.
Check existing text whose meaning changes because of the new behavior.

## Complete the review

Inspect the full effective skill definition before reporting findings.
Report findings that require a change together after the review pass is complete.
Treat a finding as requiring change when it exposes a material defect in the intended behavior, coverage, consistency, or responsibility boundary.
Treat further precision that preserves the intended behavior as optional refinement.
After reported findings are addressed, reassess the resulting definition against the same intended behavior and review criteria, and conclude the review when no material defect remains.
