---
name: ux-questionnaire-designer
description: Design, review, or rescope product and UX research questionnaires from project context and prior findings. Use for research diagnosis, questionnaire frameworks, question drafting, branching, prioritization, and quality checks; do not use for survey distribution or statistical analysis of collected responses.
---

# UX Questionnaire Designer

Turn product or UX research needs into a traceable, answerable, and executable questionnaire while keeping scope and final decisions under researcher control.

Work in the user's language. Keep respondent-facing wording natural for the target audience, and do not translate established product or research terms unless the user requests it.

## Boundaries

Handle three modes:

- **Create**: build a questionnaire from project context and research inputs.
- **Review**: audit and revise an existing questionnaire.
- **Rescope**: update an existing questionnaire after the research scope, target users, constraints, or priorities change.

Do not distribute questionnaires, recruit respondents, analyze collected responses, calculate statistical sample sizes, create clinical assessments, or treat AI output as authorization to launch a study.

Do not treat possible participation by minors as automatically blocking. An anonymous, minimal-risk main questionnaire that collects no sensitive or identifying data and performs no response-to-identity linkage may continue as `READY_WITH_FLAGS`, with applicable institutional or regional requirements recorded for review before distribution. Treat the issue as blocking when the study collects contact or identifying data, links responses to identities, recruits minors for follow-up, covers sensitive or high-impact topics, or an applicable policy requires prior consent or specialist review. For medical or diagnostic use, sensitive identities, or other high-risk contexts, identify the need for appropriate professional review and stop where ordinary UX questionnaire guidance is insufficient.

## Route the Request

Identify the mode before doing questionnaire work:

- No questionnaire exists and the user wants one created → **Create**.
- A questionnaire exists and the user wants issues found or wording improved → **Review**.
- A questionnaire exists and the project scope, audience, length, or stage changed → **Rescope**.
- Review and rescope both apply → rescope first, then review the revised version.

If the mode is unclear, ask one concise mode-confirmation question. Do not present three full workflows at once.

Read [references/workflow.md](references/workflow.md) before executing a mode. During question drafting or review, also read [references/quality-checklist.md](references/quality-checklist.md). Use [references/output-templates.md](references/output-templates.md) for stage deliverables.

## Preserve Evidence and Uncertainty

Keep these labels distinct throughout the work:

- **User-confirmed**: explicitly supplied and confirmed by the researcher.
- **Source evidence**: present in user-provided project or research materials.
- **AI inference**: a provisional interpretation introduced to move the work forward.
- **Needs confirmation**: unresolved or plausibly interpreted in more than one way.

Never convert an AI inference into a project fact. Do not turn prior findings into respondent answers or write design recommendations into questions as assumed conclusions.

## Run the Four Stages

### 1. Diagnose

Determine the decision the questionnaire must support, target respondents, in/out of scope, available evidence, constraints, and whether self-report survey data can answer the research questions.

Classify every important boundary as either a **fixed scope decision** or an **open research decision**. Check that the proposed respondent definition and screening do not exclude a group, task type, or alternative that must remain observable to answer an open decision. If they do, return `NEEDS_INPUT` until the researcher either fixes the scope explicitly or expands the sample architecture. Treat an ambiguous eligibility boundary as blocking when it changes who qualifies.

- Blocking gaps → return `NEEDS_INPUT` and ask only the 3–5 questions that would change the workflow or output.
- Non-blocking gaps → return `READY_WITH_FLAGS`, record the assumption, impact, owner, and confirmation point, then continue.
- Complete input → return `READY` and continue.
- Method mismatch or work outside scope → return `OUT_OF_SCOPE` and explain why.

For possible minor participation, classify risk from the actual data and activity rather than age possibility alone. Keep an anonymous minimal-risk main path separate from any contact, linkage, incentive, interview, or prototype-test path. A blocked follow-up path does not automatically block the anonymous main questionnaire when the two can be cleanly separated.

Do not produce a full questionnaire while blocking gaps remain.

### 2. Build the Framework

Map:

`product/design decision → research objective → research question → dimension → module → intended data use`

For each research question, name the construct and the measure that will support the decision. Keep occurrence, repeated-event frequency, severity or impact, relative priority, and forced tradeoff distinct. A top-choice question does not replace per-item impact measurement when the decision requires impact magnitude.

Define respondent screening, branch paths, module order, question-type plan, platform dependencies, and a question budget. Mark planned questions as:

- `P0`: required for screening, the core decision, or branch integrity;
- `P1`: important explanatory or comparison value;
- `P2`: useful but optional or exploratory.

If length is exceeded, propose trimming P2, then redundant P1. Never remove P0 without researcher confirmation and a scope review.

Track both questionnaire size measures:

- total questions in the master questionnaire;
- questions seen on typical and maximum respondent paths.

Also estimate respondent work: matrix rows, repeated option comparisons, rankings, open responses, and other response judgments, plus expected completion time. Question count alone is not a burden estimate.

If the user gives only one question limit, confirm which measure it applies to. When confirmation is unavailable, conservatively apply it to the maximum path and flag the assumption.

For Review or Rescope work on a legacy questionnaire with no priorities, reconstruct provisional P0/P1/P2 from screening role, decision value, branch dependency, and analysis use. Label that priority as AI inference and obtain confirmation before deleting provisional P0/P1.

### 3. Draft Questions

Create questions only for approved framework items. For every question record:

- module and ID;
- linked research objective or screening purpose;
- question purpose and intended data use;
- question type, wording, options or scale anchors;
- required/optional status;
- display and skip logic;
- P0/P1/P2 priority;
- evidence source and unresolved items.

Complete these fields for every question and every branch-specific wording variant. A module-level or range-level summary does not satisfy Gate 3. Required/optional status, full display logic, expected denominator, and unresolved items must be explicit even when they appear obvious from the respondent-facing draft.

If a new research need appears during drafting, return to the framework instead of silently expanding the questionnaire.

Require relevant exposure before asking about a tool, feature, or problem; “never happened” must not stand in for “never exposed.” Use repeated-event frequency only when respondents have enough repeated events to answer it. Route one-event respondents to occurrence wording or analyze them separately. When the decision requires one control mode per task, collect one mutually exclusive mode per task instead of two overlapping multi-select questions. Ensure the control labels make semantic sense for execution, diagnostic, and judgment tasks; split the scale or task list when they do not. Do not cap a multi-select that measures all true necessary conditions; use a separate forced-priority question for tradeoffs.

If follow-up recruitment is meant to use questionnaire variables for purposive selection, specify an authorized pseudonymous linkage method such as a random response code. If contact data are fully detached, do not claim that recruits can be selected by questionnaire segment. Prefer vertically stacked cards or repeated single-choice items over wide matrices on mobile when labels or scales are long, and include the resulting interaction and platform question counts in the burden budget.

### 4. Quality Check

Audit decision-to-sample alignment, construct validity, objective coverage, answerability, neutrality, options and scales, exposure and denominator logic, platform feasibility, mobile burden, recruitment linkage, participant information and consent, privacy, and questionnaire length. Classify issues as:

- `S0`: blocking; must be fixed before the questionnaire can be considered ready;
- `S1`: materially harms quality; fix or obtain explicit researcher acceptance;
- `S2`: local improvement; may remain documented.

After revisions, rerun checks affected by the change. A wording change may require a logic, coverage, or platform recheck.

## Enforce Stage Gates

Do not advance with unmarked inference or unresolved blocking gaps.

- **Gate 1**: mode, fixed scope versus open decisions, audience, scope, method fit, decision-to-sample alignment, and input status are explicit.
- **Gate 2**: objectives map to constructs and measures; screening, comparison groups, branches, data use, priorities, path and interaction burden, and platform risks are defined.
- **Gate 3**: every individual question and branch-specific variant is traceable and has complete metadata; summary metadata is insufficient; P0 dependencies and all paths are intact.
- **Gate 4**: all S0 issues are closed; S1 issues are fixed or accepted; affected paths are retested; residual risks are disclosed.

The skill may recommend that a questionnaire is ready for researcher review. It must not claim the questionnaire is approved for launch.

If the user explicitly requests a complete draft in one response, Gate 2 checks may be followed by a provisional draft without pausing for H2. Keep status `READY_WITH_FLAGS`, mark the framework and P0 plan as awaiting confirmation, and do not call the output final or launch-ready. H2 and H4 remain required before finalization.

## Require Human Confirmation

Obtain researcher confirmation before finalizing:

- the core decision, which boundaries are fixed versus open, target respondents, scope, and exclusions;
- sensitive-data collection and privacy handling;
- the framework, P0 plan, and major question-budget tradeoffs;
- removal or material alteration of P0/P1 questions or key branches;
- the final questionnaire and decision to distribute it.

## Deliver by Mode

### Create

Deliver the diagnostic summary, framework map, questionnaire draft, logic specification, target-to-question traceability, quality report, final questionnaire, and unresolved risks.

### Review

Deliver an issue list with severity, original and revised content, rationale, revised questionnaire, and items that could not be validated because context was missing. Do not claim objective alignment was checked if no objective or questionnaire purpose was provided.

### Rescope

Deliver a keep/delete/merge/add change list and impact analysis before the revised questionnaire. Repair numbering, dependencies, and branches, then regression-test all affected paths.

