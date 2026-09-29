# Workflow

Use this workflow after selecting Create, Review, or Rescope mode.

## States

- `READY`: current stage has no blockers.
- `READY_WITH_FLAGS`: work may continue with explicitly recorded non-blocking gaps.
- `NEEDS_INPUT`: a blocking gap requires researcher input.
- `OUT_OF_SCOPE`: the task requires another method, specialist, or capability.

When pausing, report the current mode and stage, confirmed information, blocker and impact, minimum information needed, and the node from which work will resume. After new information arrives, update the diagnostic summary before resuming. Preserve unaffected confirmed work.

## Entry Routing

1. Inventory the user request, attachments, existing questionnaire, and project materials.
2. Mark missing, unreadable, conflicting, or version-ambiguous materials.
3. Select the mode:
   - Create: no questionnaire; user wants one built.
   - Review: questionnaire exists; user wants it audited or rewritten.
   - Rescope: questionnaire exists; audience, scope, stage, length, or priorities changed.
4. If review and rescope both apply, rescope first and review the result.

## Stage 1: Diagnose

### D1. Structure Inputs

Extract:

- product/service and context;
- decision the research must support;
- fixed scope decisions already made versus open research decisions still requiring comparison;
- target respondents and exclusions;
- in-scope and out-of-scope topics;
- prior evidence;
- hypotheses to validate;
- length, platform, sample, timeline, privacy, and wording constraints.

Label each item User-confirmed, Source evidence, AI inference, or Needs confirmation.

### D2. Apply the Mode Contract

**Create requires** project context, decision, provisional audience, scope, and prior evidence or an explicit statement that none exists.

**Review requires** the current questionnaire, review focus, and the known research objective or use. A limited wording and logic review may proceed without an objective, but objective alignment cannot be claimed.

**Rescope requires** the current questionnaire, confirmed change, and what must remain or be excluded.

Treat missing decision, undefined audience, contradictory scope, unavailable current questionnaire, ambiguous active version, or an eligibility boundary that materially changes the sample as blocking when the selected mode depends on it.

Also treat a decision–sample circularity as blocking: if the study intends to decide which audience, task type, channel, or use case should be prioritized, the screening plan must not remove the alternatives before they can be compared. The researcher must either confirm the choice as a fixed scope boundary or expand the sample and analysis plan.

Prior research, platform, target length, or sample size may be non-blocking. Record a conservative default and risk instead of silently inventing them.

Possible participation by minors is not automatically blocking. If the main questionnaire is anonymous, minimal-risk, collects no sensitive or identifying data, and has no response-to-identity linkage, allow framework and drafting work to continue as `READY_WITH_FLAGS` while flagging applicable institutional or regional review before distribution. Block only the affected path when contact details, identity linkage, incentives, follow-up recruitment, sensitive topics, high-impact decisions, or an applicable rule requires prior consent or specialist review. If the main and follow-up paths can be separated, do not let an unresolved recruitment path unnecessarily block the anonymous main questionnaire.

### D3. Check Method Fit

Ask whether respondents can recall and self-report the target information. Separate self-reported behavior, experience, difficulty, attitude, and expectation from actual performance, causality, hidden behavior, and long-term change.

- Survey fits → continue.
- Survey answers only part → narrow the survey objective and flag other methods.
- Survey clearly does not fit or the work is high-risk/out of scope → `OUT_OF_SCOPE`.

### D4. Check Consistency

Verify that decision, objectives, respondents, scope, evidence, and constraints can coexist.

For every open decision, ask whether the planned sample contains the comparison groups needed to answer it. Use one of two valid paths:

- **Fixed-boundary path:** the audience/task/channel is already selected. Treat it as scope, remove claims that the questionnaire will decide it, and study needs within that boundary.
- **Comparative path:** the choice remains open. Include the relevant alternatives, define grouping variables, and plan an interpretable comparison.

Do not let a preselected sample validate its own priority. If the requested scope cannot fit the time or length, propose prioritization. Do not make the final scope decision.

### D5. Ask Minimum Necessary Questions

When blocked, ask 3–5 questions ordered by decision, audience, scope, constraints, then secondary details. Do not ask for information already available in supplied materials. Return `NEEDS_INPUT` and stop before framework generation.

### D6. Output Diagnostic Summary

Use the diagnostic template. Gate 1 passes only when mode is known, blockers are zero, fixed boundaries and open decisions are separated, decision–sample alignment is valid, method fit is checked, non-blocking gaps are registered, and no inference is unmarked.

## Stage 2: Build Framework

### F1. Establish the Objective Hierarchy

Translate the core decision into a small set of research objectives. Break them into survey-answerable research questions. Keep prior evidence separate from hypotheses. Mark core versus exploratory questions.

Return to Stage 1 if the objective or scope materially changes.

### F2. Build the Research Map

For each research question define the construct, dimensions, measure, data needed, respondent path, intended analysis use, and effect on the later product/design decision.

Keep distinct constructs separate unless the research plan explicitly justifies combining them. In particular, distinguish:

- occurrence from repeated-event frequency;
- frequency from impact severity;
- absolute necessity from relative priority;
- preference from willingness to trade off;
- no exposure from exposure without occurrence.

### F3. Design Screening and Paths

Define inclusion, exclusion, grouping, early termination, and experience-based branches. Distinguish screening variables from analysis groups and ordinary background data. For every open audience or scope decision, preserve the comparison groups needed to answer it. Flag sparse branch risk when sample information is unknown.

### F4. Organize Modules

Default sequence:

1. screening and recent experience;
2. behavior and context;
3. difficulties and decision process;
4. judgments and reasons;
5. feature or concept expectations after relevant experience;
6. background questions where they least influence core responses.

Change the order when the research objective requires it and record the reason.

### F5. Plan Data Use and Question Types

For each research question define whether the data will describe, screen, segment, cross-tab, rank, or explain. Choose question types to serve that use. Do not choose a type because a platform happens to support it.

### F6. Budget and Prioritize

Estimate module count and burden. Track master-question count, typical/maximum path count, and approximate response judgments. Count matrix rows, repeated item evaluations, ranking operations, long option scans, and open responses as interactions rather than treating each screen as one unit. If a user gives one limit without defining the measure, ask which measure it applies to; if that cannot be confirmed, use the maximum path as the conservative limit and flag the assumption.

Mark P0/P1/P2 and dependencies. For a legacy questionnaire without priorities, reconstruct provisional priorities from screening role, core-decision value, branch dependency, and intended analysis use. Label them AI inference and obtain researcher confirmation before deleting provisional P0/P1.

If over budget:

1. remove or combine P2;
2. remove redundant P1;
3. ask the researcher to choose among remaining P1;
4. if P0 must be removed, return to Stage 1 and reduce scope.

### F7. Check Feasibility

Check platform support, mobile presentation, branch complexity, likely data sparsity, and the plausibility of the stated time limit. When completion time is a requirement, require a timed pilot and report the median and range; do not infer duration from question count alone. With no platform information, use portable structures and flag dependencies.

### F8. Output Framework

Use the framework template. Gate 2 requires coverage of core questions, valid decision–sample alignment, explicit constructs and measures, module purposes and entry conditions, screening and branches, data-use plan, priorities, response-burden estimate, platform risks, and researcher confirmation of scope/P0 tradeoffs.

If the user explicitly requests a complete one-response draft, run the Gate 2 checks and then allow a provisional draft with status `READY_WITH_FLAGS`. Mark H2, the framework, and the P0 plan as pending confirmation. This exception does not permit a final or launch-ready status.

## Stage 3: Draft Questions

### T1. Create Question Slots

Create question slots from the approved framework. Define purpose, priority, data use, and dependencies before wording.

### T2. Select Types

- one category → single choice;
- multiple coexisting conditions → multiple choice;
- frequency, degree, or agreement → anchored scale;
- repeated objects on identical dimensions → matrix only after burden/platform checks; when mobile labels or anchors are long, prefer vertically stacked cards or repeated single-choice items;
- unanticipated detail → open text;
- relative priority → ranking with controlled option count.
- one control mode per task → mutually exclusive single-choice matrix or repeated single choice.

### T3. Write the Stem

Check one object, explicit and consistent reference event, clear experience condition, understandable language, neutral framing, respondent knowledge, and one main judgment. Test every matrix row or repeated item as if it were a standalone question; split rows that combine distinct problems, causes, or product responses. Split double-barreled questions. Add eligibility paths when not everyone has the experience. Do not combine multiple qualifying conditions in a screener unless satisfying any one of them is intentionally equivalent.

### T4. Write Options and Scales

Keep one conceptual level, check mutual exclusivity and coverage, provide appropriate exits, distinguish no exposure, exposed-but-not-occurred, not applicable, unable to judge, and prefer not to answer where analytically necessary, and anchor scales clearly. Do not conflate categories such as rule-based automation and generative AI when later interpretation depends on the difference. For control-level questions, verify that every label is meaningful for each row; execution verbs may not fit diagnostic or judgment tasks. Split task families or use a neutral result/next-step formulation when needed. Use response caps for forced priority, not for exhaustive necessary-condition or threshold questions. Mark unsupported option sets as AI proposals requiring review.

### T5. Specify Logic

For every conditional question record source question, trigger option, displayed question, destination, false path, required status, choice limits, and expected denominator. Gate exposure-dependent questions before measuring outcomes, and keep non-users out of the occurrence-rate denominator. If a respondent has only one eligible event, ask whether the issue occurred in that event rather than forcing a repeated-event frequency scale; do not compare the two measures as equivalent without an explicit analysis rule. If follow-up recruitment uses questionnaire variables, define explicit consent and a pseudonymous linkage key; if contact details are fully detached, limit recruitment claims accordingly. When minors may enter an anonymous main questionnaire, isolate any contact or follow-up branch and require the applicable adulthood or consent check only for that branch unless policy requires a broader restriction.

### T6. Complete Metadata

Use the question metadata template. Create one complete row for every question and every branch-specific wording variant. Do not replace individual rows with a module-level or question-range summary. Required status, full display/skip logic, expected denominator, data use, source label, and unresolved items are mandatory Gate 3 fields.

### T7. Check Each Module

Check duplication, orphan questions, expectation questions without experience evidence, priming order, hidden interaction burden, mobile presentation, recruitment-linkage claims, participant information and consent, and missing no-exposure/no-experience paths. If student or youth participation is possible, distinguish the anonymous minimal-risk main path from contact, identity-linkage, interview, and prototype-test paths. Confirm the applicable age and consent rule before activating any affected path; do not automatically block an otherwise separable anonymous main questionnaire. Return to the framework when the issue is structural.

### T8. Output Draft

Create mode-specific additions:

- Review: original, issue, revision, rationale.
- Rescope: change type and all affected questions/paths.

Gate 3 requires full traceability, one complete metadata row per question and branch-specific variant, intact P0 dependencies, explicit branch entry/exit, no silently added research questions, and a consolidated confirmation list. A metadata summary by question range does not pass Gate 3.

## Stage 4: Quality Check

Read `quality-checklist.md` and run all applicable checks.

Classify findings:

- S0: blocks readiness;
- S1: material quality risk; fix or obtain explicit acceptance;
- S2: local improvement.

Use these return paths:

- decision, audience, or scope → Stage 1;
- research question, sample architecture, module, budget → Stage 2;
- type, wording, options, or local logic → Stage 3.

After each change, rerun affected coverage and path checks. Gate 4 requires all S0 closed, S1 fixed or explicitly accepted, affected paths retested, platform limits checked or disclosed, and residual risks consolidated.

## Human Confirmation Points

- H1: fixed versus open decisions, audience, scope, comparison groups, exclusions, sensitive data.
- H2: research questions, modules, P0 plan, sample branches, major budget tradeoffs.
- H3: removal or material change of P0/P1, core scales, or key branches.
- H4: final questionnaire and decision to distribute.

