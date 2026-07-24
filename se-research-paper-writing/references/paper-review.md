# Paper Review Guide

## Goal

Review an SE paper as a skeptical program committee member before submission. Identify rejection risks early and revise claims, evidence, and presentation accordingly.

## Reviewer Core Questions

1. SE relevance: Is the paper solving a real software engineering problem?
2. Paper type: Is the paper clearly a Tool Paper or an Empirical Study?
3. Story alignment: Do Abstract, Introduction, Methodology, Evaluation, Discussion, and Conclusion tell the same story?
4. Background sufficiency: Are concepts, problem statement, and threat model clear enough?
5. Challenge-method alignment: Does each challenge map to a method or study design?
6. RQ-evidence alignment: Does each RQ receive direct evidence?
7. Evidence strength: Do datasets, baselines, metrics, numbers, qualitative findings, or case studies support the claims?
8. Discussion and threats: Are limitations specific and reflected in claim wording?
9. Reproducibility: Are artifacts, datasets, scripts, prompts, or protocols available or sufficiently described?
10. Clarity: Can reviewers summarize the contribution after one reading?

## Claim-Evidence Audit

For every major claim in Abstract and Introduction, write:

`Claim: ... | Evidence: ... | Section/Table/Figure: ... | Threat/Boundary: ... | Status: supported/needs evidence/overclaimed`

## Challenge-Method-Evaluation Audit

For every challenge or RQ, write:

`Challenge/RQ: ... | Method/Study Design: ... | Evaluation Evidence: ... | Discussion/Threat: ... | Status: aligned/missing/overclaimed`

## Common Rejection Risks

1. Paper type is unclear: the work is neither a convincing tool paper nor a convincing empirical study.
2. Background is too thin for reviewers to understand the task or threat model.
3. Motivating example does not demonstrate why current solutions fail.
4. Challenges are listed but not addressed by Methodology.
5. Methodology lacks an overview or input-output workflow.
6. Evaluation lacks experimental setup or is not organized by RQ.
7. Results use vague claims without concrete numbers or evidence.
8. Discussion contains generic threats rather than claim-specific boundaries.
9. Related Work lists papers without positioning.
10. Conclusion overstates implications beyond the evidence.

## Adversarial Review Workflow

1. Write the harshest plausible reviewer summary.
2. List the top five reasons for rejection.
3. Map each reason to a fix: rewrite, add evidence, weaken claim, clarify threat, improve positioning, or restructure a section.
4. Revise the paper and repeat until no high-risk issue remains unresolved.