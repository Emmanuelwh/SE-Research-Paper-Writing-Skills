# Paper Review Guide

## Goal

Review an SE paper as a skeptical program committee member before submission. Identify rejection risks early and revise claims, evidence, and presentation accordingly.

## Reviewer Core Questions

1. SE relevance: Is the paper solving a software engineering problem, not only applying a technique to code data?
2. Novelty: What is new compared with prior SE work and current practice?
3. Significance: Who benefits, and is the benefit important enough for the venue?
4. Methodological soundness: Are RQs, subjects, data collection, metrics, baselines, and analysis justified?
5. Evidence strength: Do results support the claims at the right scope?
6. Validity: Are threats identified, mitigated, and reflected in claim wording?
7. Reproducibility: Are artifacts, datasets, scripts, prompts, or protocols available or sufficiently described?
8. Clarity: Can reviewers summarize the paper's story after one reading?

## Five-Dimension Self-Review

### 1) Contribution

1. What exactly is contributed: finding, tool, technique, benchmark, dataset, taxonomy, theory, or replication?
2. Is each contribution named in the Introduction and supported later?
3. Are contribution boundaries explicit?

### 2) Writing Clarity

1. Does each section have one clear role?
2. Does each paragraph have one message?
3. Are RQs, terms, metrics, and claims consistent across sections?

### 3) Methodology Soundness

1. Are RQs answerable with the chosen study design?
2. Are subject selection and filtering criteria justified?
3. Are labels, metrics, baselines, and procedures valid?

### 4) Evaluation Completeness

1. Does each RQ receive direct evidence?
2. Are baselines and comparisons fair?
3. Are statistical, qualitative, or case-study analyses appropriate?
4. Are failure cases and negative results explained?

### 5) Validity and Reproducibility

1. Are construct, internal, external, and conclusion validity threats discussed when applicable?
2. Are claims scoped according to the evidence?
3. Can another researcher replicate or inspect the artifact/study?

## Claim-Evidence Audit

For every major claim in Abstract and Introduction, write:

`Claim: ... | Evidence: ... | Section/Table/Figure: ... | Threat: ... | Status: supported/needs evidence/overclaimed`

Revise all `overclaimed` statements before finalizing.

## Common SE Rejection Risks

1. The paper lacks a clear SE problem and reads like generic ML/AI applied to software artifacts.
2. RQs are listed but do not structure Methodology and Evaluation.
3. Dataset or benchmark construction is underspecified.
4. Metrics are convenient but not valid proxies for the claimed construct.
5. Baselines are weak, outdated, unfair, or missing.
6. Threats to validity are generic and do not bound the actual claims.
7. Contributions are stated as novelty claims without evidence of usefulness or insight.
8. The artifact is central but not available or not described enough to evaluate.
9. Related Work lists papers but does not establish the gap.
10. Abstract/Introduction claims are stronger than Evaluation supports.

## Adversarial Review Workflow

1. Write the harshest plausible reviewer summary.
2. List the top five reasons for rejection.
3. Map each reason to a fix: rewrite, add evidence, weaken claim, clarify threat, or improve positioning.
4. Revise the paper and repeat until no high-risk issue remains unresolved.
