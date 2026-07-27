# Experimental Setup Example

Use this example when writing the opening setup of a Tool Paper Evaluation section.

## Setup Skeleton

```latex
\subsection{Experimental Setup}

\textbf{Dataset.}
We constructed our dataset from [source] because [reason tied to the paper's target setting]. We collected [subjects/cases/artifacts] from [time window/search process/benchmark source]. We included [criteria] and excluded [criteria] to ensure [quality/objectivity]. To reduce selection bias, we [sampling strategy/diversity control/multiple data sources]. The final dataset contains [scale], covering [projects/ecosystems/case types/severities/versions]. Ground truth was obtained by [source/manual labeling/reproduction/developer confirmation], and disagreements were resolved by [procedure].

\textbf{Metrics.}
We evaluate [Tool] using [metric 1], [metric 2], and [metric 3]. [Metric 1] measures [construct], where higher/lower is better. [Metric 2] captures [construct] because [reason]. For real-world usefulness, we additionally report [confirmed findings/manual effort/developer response/patch status].

\textbf{Baselines.}
We compare [Tool] with [baseline 1], [baseline 2], and [baseline 3]. [Baseline 1] represents [SOTA/current practice/simple heuristic]. [Baseline 2] is included because [reason]. We run all methods on the same dataset and use the same [preprocessing/ground truth/resource budget]. When a baseline does not directly support our setting, we adapt it by [adaptation] while keeping [fairness condition] unchanged.

\textbf{Implementation and Environment.}
We implemented [Tool] in [language] using [framework/library/toolchain]. Experiments were conducted on [hardware] running [OS/runtime]. Unless otherwise stated, we used [settings, thresholds, model versions, prompts, seeds, timeouts]. We will release [code/data/scripts/container] to support replication.
```

## Dataset Objectivity Phrases

Use these only when true:

1. `To avoid cherry-picking, we selected subjects before running [Tool].`
2. `We used a fixed time window and included all projects satisfying the criteria.`
3. `We sampled projects across [ecosystems/languages/sizes] to cover diverse settings.`
4. `Two authors independently labeled [cases], and disagreements were adjudicated by [procedure].`
5. `For security findings, we manually reproduced each candidate and recorded confirmation status.`

## Metric Explanation Phrases

1. `Precision measures how many reported cases are correct, which captures inspection burden.`
2. `Recall measures how many known cases the tool finds, which captures missed-risk reduction.`
3. `Top-k precision reflects the usefulness of ranked reports under limited inspection budget.`
4. `Runtime measures whether the tool can be used at the intended project scale.`
5. `Confirmed findings measure real-world usefulness beyond benchmark performance.`

## Common Fixes

1. If the dataset paragraph only reports counts, add collection criteria and ground-truth protocol.
2. If metrics are listed without meaning, explain what each metric measures in SE terms.
3. If baselines are named without justification, say what each baseline represents.
4. If implementation details repeat Methodology, keep only experimental configuration and reproducibility settings.