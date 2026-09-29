# Quality Checklist

Use during question drafting, review, rescoping regression checks, and final quality assurance.

## Severity

- Assign severity from impact, not from the issue label alone. First ask whether the issue makes a core objective unanswerable, selects the wrong sample, breaks a path, systemically distorts a core measure, or prevents implementation.
- **S0 blocking**: causes one of those study-level failures or violates a required constraint.
- **S1 important**: materially reduces interpretation consistency, data quality, or analysis value.
- **S2 improvement**: affects local clarity, efficiency, or presentation without invalidating the study.

A locally repairable leading or double-barreled question is usually S1. Raise it to S0 only when it systemically distorts a core measure or leaves the core objective without a valid replacement.

## 1. Objective Coverage

- Are fixed scope boundaries separated from open research decisions?
- For every open decision, does the sample preserve the alternatives or comparison groups needed to answer it?
- Is a preselected audience, task type, or channel being used to "prove" that the same audience, task type, or channel should be prioritized?
- Does any ambiguous eligibility definition materially change who enters the sample? If yes, treat it as blocking.
- Does every core research question have the data needed to answer it?
- Does every non-screening question map to a research objective or research question?
- Are screening-only questions marked as such?
- Are obsolete questions left after a scope change?
- Is a feature-expectation answer being used as a substitute for evidence about real behavior or difficulty?
- Are design recommendations embedded as assumed conclusions?

Return structural gaps to the framework stage.

## 2. Answerability

- Can the target respondent know or recall the answer?
- Is the recall period plausible for the event frequency?
- Is the reference event consistent across screening, behavior, and follow-up questions?
- Does a repeated-event frequency scale exclude or reroute respondents with only one eligible event?
- Does the respondent need an experience condition before answering?
- Is one main judgment requested at a time?
- Has every matrix row or repeated item been checked as a standalone question for combined problems, causes, or outcomes?
- Are terms understandable without domain expertise?
- Does the question ask the respondent to predict other people, markets, or distant future behavior?
- Are hypothetical feature questions grounded in a described scenario?

## 3. Neutrality and Bias

- Does the stem imply the expected or desirable answer?
- Does it assume the product or feature is valuable, effective, or already needed?
- Are positive and negative scale anchors balanced?
- Does provided concept information include only what is needed for a fair judgment?
- Could prior questions prime or educate the respondent in a way that changes later answers?
- Are socially desirable answers made unusually easy or prominent?

## 4. Options and Scales

- Are single-choice options mutually exclusive?
- Do multiple-choice options cover major plausible cases?
- Are options at the same conceptual level and time frame?
- Are Other, Unsure, Not experienced, Not applicable, and Prefer not to answer used only where needed?
- Does the scale have clear anchors and direction?
- Is scale direction consistent across similar questions?
- Are option counts practical for mobile display and platform limits?
- Are multi-select choice limits justified?
- Is an exhaustive necessary-condition or adoption-threshold question uncapped, with forced priority measured separately?
- Are occurrence, frequency, impact, priority, necessity, and tradeoff treated as distinct constructs?
- When one control mode per task is required, are the response modes mutually exclusive?
- Do control-mode labels make semantic sense for execution, diagnostic, and judgment rows, or should the task families use different scales?
- Are analytically different categories, such as rule-based automation and generative AI, kept distinct when needed?

## 5. Branch and Denominator Integrity

For every branch verify:

- source question;
- trigger option;
- displayed question;
- false path;
- destination or end;
- no dead end, loop, duplicate display, or unreachable node;
- denominator can be explained in reporting.
- exposure-dependent questions exclude unexposed respondents from the outcome denominator.

Simulate at least:

- eligible respondent with complete experience;
- eligible respondent missing one experience;
- ineligible respondent;
- every major branch;
- Other/Unsure/Not applicable;
- old paths affected by rescoping.

## 6. Burden and Priority

- Is the questionnaire within the stated length/time budget?
- Are total master-question count and typical/maximum path counts reported separately?
- Is approximate response-judgment count reported, including matrix rows, repeated item ratings, ranking operations, long option scans, and open responses?
- If only one question limit was supplied, is its interpretation confirmed or conservatively flagged?
- Are open, ranking, matrix, and high-recall questions limited?
- Are repeated measures necessary?
- Are P0 dependencies intact?
- Were cuts proposed in the order P2, redundant P1, researcher-approved P1?
- If P0 must be cut, was the task returned to scope review?
- For a legacy questionnaire, were provisional priorities reconstructed and labeled as AI inference before cuts?
- When completion time is constrained, was a timed pilot conducted and were median and range recorded rather than inferred from question count?

## 7. Platform and Analysis Feasibility

- Can the target platform implement each type, option count, randomization, matrix, quota, and skip rule?
- Is the mobile experience acceptable?
- When labels or scale anchors are long, is a vertical card or repeated single-choice presentation used instead of a wide mobile matrix?
- Will branching or subgroup comparison likely create sparse data?
- If the study asks which audience, task type, or channel to prioritize, is there a viable comparison group and analysis plan?
- Does every non-screening question state its intended data use?
- Is each background variable included for a specific segmentation, representativeness, or recruitment use rather than as a fixed demographic checklist?
- Can the planned data actually support that use?
- Are platform-unknown dependencies disclosed rather than assumed?

Do not perform statistical sample-size calculation under this skill. Flag the need when relevant.

## 8. Privacy and Research Ethics

- Is each personal or sensitive field necessary for a research objective?
- Is purpose clear and is a reasonable exit available?
- Does the introduction state the study purpose, voluntary participation, withdrawal/exit option, expected duration or an honest unverified estimate, intended data use, and privacy handling?
- If follow-up participants will be selected using questionnaire variables, is there explicit consent and a pseudonymous linkage key? If not, are purposive-segment recruitment claims removed?
- Are unrelated private details excluded?
- Are minors, medical/diagnostic use, sensitive identities, or high-impact decisions involved?
- If minors may participate, is the anonymous minimal-risk main path separated from contact collection, identity linkage, incentives, follow-up interviews, and prototype testing?
- Is minor participation being classified from the actual data and activity rather than blocked solely because age is uncertain?
- Before an affected path is activated, is the applicable adulthood threshold and any required guardian/participant consent process explicit?
- Is specialist review required?

## 9. Final Consistency

- Numbering and references are correct.
- Terminology and time windows are consistent.
- Required/optional settings match the intended path.
- Changes are reflected in the framework, metadata, logic table, and final questionnaire.
- Does every individual question and branch-specific wording variant have a complete metadata row rather than only a range-level summary?
- AI inferences and unresolved items are consolidated.
- Fixed scope choices are not presented as findings generated by the questionnaire.
- The output says “recommended for researcher review,” not “approved to launch.”

