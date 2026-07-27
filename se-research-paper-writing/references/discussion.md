# Discussion, Limitations, and Threats to Validity Guide

## Goal

Use this guide to write the paper section that interprets results, scopes claims, and states threats to validity. In this SE skill, Threats to Validity is required, while other discussion sections are optional. The required threats should be concise and organized only as External Validity and Internal Validity.

Do not split threats into construct, conclusion, reliability, or many venue-style categories. If those issues matter, fold them into either External Validity or Internal Validity based on the claim they affect.

## Recommended Section Structure

Use this default structure:

1. Optional Discussion or Implications: explain what the results mean for researchers, practitioners, tool builders, auditors, maintainers, or benchmark designers.
2. Optional Practical Deployment: discuss adoption, integration, runtime, cost, manual effort, disclosure workflow, user burden, or operational constraints.
3. Optional Limitations: state method boundaries, unsupported settings, assumptions, negative results, and failure cases.
4. Required Threats to Validity: include External Validity and Internal Validity.
5. Optional Ethical or Security Considerations: discuss responsible disclosure, privacy, sensitive artifacts, exploit risk, generated code risk, or misuse when relevant.
6. Optional Future Work: state concrete next steps that follow from limitations or threats.

If page limit is tight, keep only a short Discussion paragraph plus the required Threats to Validity subsection.

## Discussion vs. Threats to Validity

Use Discussion for interpretation: what the results imply, how the tool or study may be used, and why findings matter.

Use Limitations for method or scope boundaries: what the tool cannot handle, where assumptions may fail, or which settings remain unsupported.

Use Threats to Validity for risks to the evidence behind the claims: whether the evaluation setting, data, labels, baselines, metrics, implementation, or analysis could weaken the conclusion.

Do not duplicate the same issue in all three places. If an issue affects the claim's scope, put it in Limitations. If it affects the trustworthiness of the evidence, put it in Threats to Validity.

## Required Threats to Validity Structure

Only use these two categories.

### External Validity

External validity discusses whether results generalize beyond the evaluated subjects, settings, and scenarios.

Typical issues:

1. Dataset, benchmark, project, ecosystem, language, platform, or version representativeness.
2. Generalization to unseen projects, larger systems, noisier data, different workflows, or different user groups.
3. Real-world deployment differences from the experimental setting.
4. Temporal validity when tools, APIs, repositories, attacks, or developer practices change over time.
5. Security or reliability setting differences, such as different threat models, attacker behavior, vulnerability classes, or operational environments.

Writing pattern:

`External validity concerns whether our results generalize beyond [evaluated scope]. Our evaluation covers [coverage evidence], which reduces this threat by [reason]. However, the results may differ for [unstudied settings], so our claims should be interpreted within [bounded scope].`

### Internal Validity

Internal validity discusses whether the reported results are trustworthy for the evaluated setting and whether alternative explanations could account for them.

Typical issues:

1. Ground truth quality, manual labeling, coder disagreement, oracle correctness, or reproduction errors.
2. Baseline fairness, baseline configuration, reimplementation differences, or protocol mismatch.
3. Metric choice, proxy measurement, annotation protocol, prompt variability, random seeds, thresholds, or model nondeterminism.
4. Implementation bugs, parser limitations, tool crashes, incomplete data, missing metadata, or preprocessing errors.
5. Confounding factors in ablations, user studies, case studies, or real-world validation.
6. Statistical uncertainty, small sample size, qualitative interpretation, or insufficient repeated trials.

Writing pattern:

`Internal validity concerns whether [result/claim] is affected by [possible bias or confounder]. We mitigate this risk by [control, fixed protocol, manual verification, multiple annotators, official baseline implementation, repeated runs, sensitivity analysis, or artifact release]. Nevertheless, [remaining uncertainty] may remain, and the result should be interpreted as [bounded conclusion].`

## How to Fold Other Threat Types into Two Categories

Do not create extra headings. Fold issues as follows:

1. Construct validity issues usually belong under Internal Validity because they concern whether metrics, labels, tasks, or proxies support the evaluated claim.
2. Conclusion validity issues usually belong under Internal Validity because they concern statistical or interpretive reliability of reported results.
3. Reliability and reproducibility issues usually belong under Internal Validity because they concern whether the experimental protocol and implementation support the result.
4. Generality issues belong under External Validity because they concern scope beyond evaluated subjects.
5. Ethical and security issues should be a separate optional section only when they concern responsible conduct or misuse rather than validity of evidence.

## Threat Writing Pattern

For each threat paragraph, include:

1. Threat: what could weaken the claim?
2. Affected claim: which result or conclusion is at risk?
3. Mitigation: what did the paper do to reduce the risk?
4. Remaining boundary: what uncertainty remains?

Compact pattern:

`[Threat] may affect [claim]. We mitigate this risk by [mitigation]. However, [remaining boundary], so our conclusion should be interpreted within [scope].`

## Optional Discussion Sections

### Implications

Use when results support lessons for researchers, practitioners, tool builders, auditors, maintainers, or benchmark designers.

Pattern:

`The results suggest [implication] for [stakeholder]. This implication follows from [result/evidence]. It is useful because [reason], but it should be interpreted within [scope].`

### Practical Deployment

Use when the paper claims practical value or real-world adoption.

Discuss:

1. Integration into existing workflow.
2. Required inputs, runtime, cost, manual effort, or expertise.
3. How users should interpret or act on the output.
4. Responsible disclosure or operational safety when relevant.
5. Failure modes users should watch for.

### Limitations

Use when the method has known boundaries that are not merely evaluation threats.

Pattern:

`[Tool/Study] currently does not handle [setting/case]. This limitation arises because [reason]. As a result, [claim] should be limited to [scope]. Addressing this limitation would require [future direction].`

### Ethical or Security Considerations

Use only when relevant. For security papers, discuss responsible disclosure, sensitive data, exploitability, and misuse. For developer-data papers, discuss privacy, anonymization, consent, and data handling.

## Writing Rules

1. Threats to Validity is required; optional sections should appear only when they add concrete value.
2. Use only External Validity and Internal Validity headings for threats.
3. Do not use generic threats that could fit any SE paper.
4. Tie every threat to a concrete claim, result, dataset, metric, baseline, implementation choice, or deployment setting.
5. Include both mitigation and remaining uncertainty.
6. Do not hide major negative results or failure cases.
7. Scope Abstract and Introduction claims according to these threats.
8. Avoid over-apologizing; threats should clarify scientific boundaries, not weaken justified claims unnecessarily.

## Semi-Template

```latex
\section{Discussion and Threats to Validity}

\subsection{Discussion} % optional
[Interpret the main findings, implications, deployment value, or limitations when useful.]

\subsection{Threats to Validity} % required
\textbf{External validity.} [Discuss generalization beyond evaluated subjects/settings. Include mitigation and remaining boundary.]

\textbf{Internal validity.} [Discuss whether results are trustworthy within the evaluated setting. Include mitigation and remaining uncertainty.]
```

## Example Reference

- `references/examples/discussion-examples.md`

## Checklist

1. Is Threats to Validity present even if other discussion sections are short or omitted?
2. Are threats grouped only into External Validity and Internal Validity?
3. Are generalization issues placed under External Validity?
4. Are data, metric, baseline, labeling, implementation, and analysis issues placed under Internal Validity?
5. Does each threat name the affected claim and mitigation?
6. Are optional discussion sections included only when they add paper-specific insight?
7. Are claims in Abstract, Introduction, and Evaluation scoped according to the stated threats?