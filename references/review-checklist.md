# Review Checklist

Use this checklist when evaluating a project plan before final approval.

## Strategic Fit

- The objective is specific and measurable.
- The target user or audience is clear.
- The proposed outputs match the user's real goal.
- The project is independent from unrelated local projects unless comparison is intentional.

## Evidence

- Current or unstable facts have been verified.
- Legal or regulatory claims have authority.
- Comparable examples are real and relevant.
- Assumptions are labeled separately from facts.

## Scope

- In-scope and out-of-scope items are explicit.
- The first version is small enough to execute.
- Dependencies and blockers are visible.
- The plan does not silently add unrelated work.

## Execution Readiness

- Milestones produce concrete outputs.
- Acceptance criteria are testable.
- Roles, tools, materials, and timing are realistic.
- Risks have mitigation actions and trigger points.

## Claude Joint Review

Use this section when the user says “启动 Claude 联合评审” or when the plan is important enough to justify external review.

- Prepare a review packet containing the goal, current plan, assumptions, constraints, risks, and questions.
- Call Claude through the local CLI when available and usable.
- If Claude cannot be called, give the user a ready-to-copy prompt for Claude App.
- Ask Claude to check feasibility, missing assumptions, legal/compliance exposure, execution risks, cost/schedule realism, and better alternatives.
- Compare Claude's comments with Codex's own review instead of accepting them blindly.
- Record which Claude suggestions were adopted, rejected, or deferred.

## Decision Quality

- Alternatives were considered where useful.
- The recommended option explains tradeoffs.
- The plan states continue, pause, shrink, or reject conditions.
- User approval is required before implementation.

## Revision Guidance

When problems appear, revise in this order:

1. Fix objective and success criteria.
2. Reduce scope to a viable first version.
3. Resolve legal, data, or operational blockers.
4. Adjust milestones and resources.
5. Re-run comparison if the recommended path changes.

## Acceptance Readiness

Before implementation starts, confirm the plan defines:

- acceptance owner
- concrete deliverables
- testable acceptance criteria
- required evidence
- user-visible proof or demo
- whether Claude joint acceptance should be used after delivery

Do not treat review approval as project acceptance. Review approves the plan; acceptance verifies the delivered result.
