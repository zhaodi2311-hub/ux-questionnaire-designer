# Output Templates

Adapt these structures to the task. Do not include empty sections that add no value, but preserve fields required by the active mode and Gate.

## 1. Diagnostic Summary

```markdown
## Diagnostic Summary

- Mode: Create / Review / Rescope
- Current stage: Diagnose
- Status: READY / READY_WITH_FLAGS / NEEDS_INPUT / OUT_OF_SCOPE
- Core decision:
- Fixed scope decisions:
- Open research decisions:
- Decision–sample alignment:
- Target respondents:
- In scope:
- Out of scope:
- Prior evidence:
- Hypotheses to validate:
- Constraints:
- Method-fit conclusion:

### Source labels
| Information | Label | Source/Reason |
|---|---|---|

### Blocking gaps
| Gap | Impact | Minimum information needed |
|---|---|---|

### Non-blocking flags
| Gap | Temporary handling | Impact | Confirm by |
|---|---|---|---|

### Next step
```

If status is `NEEDS_INPUT`, ask only 3–5 questions needed to clear current blockers.

## 2. Research Framework Map

```markdown
| Decision | Research objective | Research question | Evidence or hypothesis | Construct | Dimension | Measure | Module | Respondent path | Intended data use | Priority |
|---|---|---|---|---|---|---|---|---|---|---|
```

Add:

- screening and grouping definition;
- module order and rationale;
- question budget by P0/P1/P2, including master-question total and typical/maximum path counts;
- platform dependencies;
- researcher decisions required before Gate 2.

## 3. Module Plan

```markdown
| Module | Purpose | Eligible respondents | Entry condition | Planned question types | Estimated count | Burden/risk |
|---|---|---|---|---|---|---|
```

Add a path budget:

```markdown
| Measure | Count/limit | Status or assumption |
|---|---|---|
| Master questionnaire total | | |
| Typical respondent path | | |
| Maximum respondent path | | |
| Estimated response judgments | | |
| Timed pilot: median and range | | |
```

## 4. Question Metadata

```markdown
| ID | Module | Research link | Construct/measure | Purpose | Type | Stem | Options/anchors | Required | Exposure/display/skip logic | Expected denominator | Priority | Data use | Source label | Needs confirmation |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
```

For long questionnaires, present readable respondent-facing questions first and the metadata table afterward.

Use one row per question and per branch-specific wording variant. A module-level or question-range summary does not satisfy Gate 3. Write `None` where an unresolved-item field has been checked and is empty rather than leaving it implicit.

## 5. Branch Logic

```markdown
| Source question | Trigger | Displayed question/path | False path | Destination/end | Expected denominator | Risk |
|---|---|---|---|---|---|---|
```

## 6. Review Findings

```markdown
| Finding ID | Severity | Question/module | Problem | Impact | Recommended change | Status | Researcher confirmation |
|---|---|---|---|---|---|---|---|
```

When revising wording:

```markdown
### Qx
- Original:
- Issue:
- Revised:
- Rationale:
- Checks to rerun:
```

## 7. Rescope Change List

Output this before the revised questionnaire.

```markdown
| Change ID | Type: keep/delete/merge/add | Affected question/path | Reason | Effect on objective/data/logic | Researcher confirmation |
|---|---|---|---|---|---|
```

Then include:

- new scope summary;
- revised framework impact;
- repaired numbering and branch notes;
- regression paths tested.

## 8. Final Delivery

```markdown
## Final Questionnaire

## Branch Logic

## Objective-to-Question Traceability

## Quality Summary
- S0 closed:
- S1 fixed or accepted:
- Decision–sample alignment:
- Paths retested:
- Platform checks:
- Response-burden estimate:
- Timed-pilot result:

## Residual Risks and Dependencies

## Key Changes from Draft

## Status
Recommended for researcher review / Needs further input / Out of scope
```

Never label the questionnaire approved for launch unless the researcher explicitly completes that decision outside the skill's recommendation.

