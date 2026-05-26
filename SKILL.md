---
name: project-initiation-implementation
description: Use for 项目审建一体化: project initiation, feasibility study, implementation planning, proposal drafting, solution comparison, decision review, controlled execution, and project acceptance. Automatically use in Plan mode when the task involves project scoping, research, feasibility validation, implementation方案, review, evaluation, comparable-project benchmarking, go/no-go decisions, approval-based execution, or acceptance verification. Trigger when the user proposes a project theme, asks to evaluate whether a project should be done, wants a first-version implementation plan, wants comparable-project benchmarking, asks Codex to implement only after an approved plan, or asks to验收/accept completed work.
---

# 项目审建一体化

Use this skill to run a disciplined project lifecycle for “项目审建一体化”: topic intake, research and feasibility analysis, discussion, first-version plan, review and revision, comparable-project comparison, implementation decision, execution after explicit user approval, and project acceptance.

Default to Chinese communication unless the user asks otherwise. Keep explanations plain, concrete, and decision-oriented.

## Core Rules

- Treat each project as independent. Do not mix context, files, assumptions, or implementation choices from unrelated projects unless the user explicitly asks for comparison.
- Do not implement before the user approves the final plan. If the user asks to proceed without a plan, create a short plan first and ask for confirmation.
- If current facts, market data, legal rules, products, pricing, APIs, or comparable examples matter, research and cite sources before relying on them.
- Separate confirmed facts, assumptions, open questions, and recommendations.
- Keep the user in the decision loop at the three gates: after research, after first-version plan, and before implementation.
- For legal, finance, medical, safety, or other high-stakes projects, raise evidence standards and avoid unsupported conclusions.

## Workflow

### 1. Intake the Project Theme

When the user provides a project theme, restate the theme and identify:

- project goal
- intended users or audience
- expected output
- constraints already known
- decision needed from the user
- immediate missing information

Ask only the questions needed to avoid a bad start. If reasonable assumptions are available, state them and continue.

### 2. Research and Feasibility Study

Investigate the project before drafting a solution. Cover the relevant parts:

- user need and use case
- technical feasibility
- operational feasibility
- legal and compliance constraints
- cost, schedule, and resource needs
- risks and blockers
- comparable solutions or similar projects
- success criteria

Use web research when facts may be current, contested, or important to the decision. Prefer primary and authoritative sources. For legal analysis, use real cases with case numbers when cases are needed.

### 3. Discussion Checkpoint

Before drafting the first implementation plan, summarize findings in a compact decision memo:

- what is viable
- what is risky
- what is unclear
- recommended direction
- questions for the user

Invite correction of assumptions and scope. Do not proceed to implementation at this checkpoint.

### 4. Draft Plan Version 1

Create the first-version implementation plan after research and discussion. Use `references/implementation-plan-template.md` when a structured plan is needed.

The plan should include:

- background and objectives
- scope and non-scope
- users, scenarios, and deliverables
- implementation path
- milestones and schedule
- resources and responsibilities
- budget or effort estimate when useful
- risks and mitigations
- acceptance criteria
- decision points
- next actions

### 5. Review, Evaluate, and Revise

Run a review pass with the user. Use `references/review-checklist.md` for quality control.

When the user asks to “启动 Claude 联合评审”, or when an important plan would benefit from an external second opinion, add a Claude joint-review step before finalizing revisions:

- Prepare a concise review packet for Claude: project objective, current plan, key assumptions, constraints, risks, and specific questions.
- If Claude CLI is available and authenticated, ask Claude to review the plan from feasibility, risk, implementation, and missing-assumption angles.
- If Claude cannot be called because of quota, login, network, or tool limits, provide a ready-to-copy Claude review prompt for the user to run manually.
- Treat Claude's output as advisory input, not automatic truth. Compare it with Codex's own review and the user's priorities before revising the plan.
- Summarize what was adopted, rejected, or left undecided from Claude's review.

Evaluate whether the plan is:

- aligned with the user's goal
- realistically scoped
- technically and operationally feasible
- legally and commercially defensible
- measurable through acceptance criteria
- ready for execution

Revise the plan when feedback changes scope, constraints, risk, timeline, or implementation path.

### 6. Compare Similar Projects and Decide

Before final approval, compare similar projects, products, cases, or implementation models when they exist. Use `references/comparison-framework.md` when a formal comparison is useful.

Make the comparison decision-oriented:

- what comparable example shows
- where it is better
- where it is worse
- what should be copied
- what should be avoided
- whether the project should proceed, pause, shrink, or be rejected

### 7. Implement After Approval

Only execute after the user explicitly agrees to the plan or asks to implement the approved version.

During implementation:

- follow the approved scope
- keep changes inside the relevant project directory
- report meaningful progress
- surface blockers early
- verify outputs against the acceptance criteria
- avoid expanding scope without user approval

If execution reveals that the approved plan is wrong or incomplete, pause and propose a plan amendment before continuing.

### 8. Accept and Close the Project

After implementation, run a project acceptance step before declaring the project complete.

Verify against:

- approved scope
- deliverables
- acceptance criteria
- tests or evidence
- user-visible results
- unresolved risks and known limitations
- required documents, files, or deployment outputs

When the user asks to “启动 Claude 联合验收”, or when an important completed project would benefit from an external acceptance check, add a Claude joint-acceptance step:

- Prepare an acceptance packet for Claude: approved plan, completed work summary, acceptance criteria, evidence, known limitations, and specific验收 questions.
- If Claude CLI is available and authenticated, ask Claude to independently check whether the delivered work satisfies the approved plan and acceptance criteria.
- If Claude cannot be called because of quota, login, network, or tool limits, provide a ready-to-copy Claude acceptance prompt for the user to run manually.
- Treat Claude's output as acceptance advice, not the final decision. The final验收 decision belongs to the user.
- Summarize pass/fail/conditional-pass items, fixes required before acceptance, and any Claude suggestions adopted, rejected, or deferred.

Close only after the user confirms acceptance or explicitly asks to proceed despite remaining issues.

## Output Modes

Use the mode that matches the current stage:

- **Intake note**: short restatement, assumptions, missing inputs, next research step.
- **Research memo**: sourced findings, feasibility judgment, risks, recommended direction.
- **Discussion brief**: focused questions and decisions needed from the user.
- **Implementation plan**: structured plan with milestones and acceptance criteria.
- **Review report**: issues, suggested revisions, readiness assessment.
- **Comparison matrix**: alternatives, pros/cons, decision recommendation.
- **Execution update**: what was done, evidence, remaining work, next step.
- **Acceptance report**: delivered items, evidence, pass/fail findings, remaining issues, user decision needed.

## References

- `references/implementation-plan-template.md`: load when drafting a full plan.
- `references/review-checklist.md`: load when reviewing or revising a plan.
- `references/comparison-framework.md`: load when comparing similar projects or deciding whether to proceed.
- `references/acceptance-checklist.md`: load when verifying deliverables, running project acceptance, or performing Claude joint acceptance.
