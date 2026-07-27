# Tool Paper Methodology Overview Example

Use this example when drafting the first Methodology subsection for an SE Tool Paper. Reuse the structure, not the topic.

## What the Overview Must Do

The overview should tell reviewers four things before module details:

1. What task the tool supports.
2. What the tool receives as input and produces as final output.
3. What modules appear in the complete tool figure.
4. How the following subsections explain the modules in the same order as the figure.

## Figure Planning Template

```text
Input artifacts
  -> Module 1: [extract/collect/normalize/construct]
     Output: [intermediate representation]
  -> Module 2: [analyze/infer/match/rank/generate]
     Output: [candidate result]
  -> Module 3: [validate/filter/explain/report/repair]
     Output: [final actionable output]
```

Figure caption pattern:

`Figure X overviews [Tool]. Given [inputs], [Module 1] produces [artifact 1], [Module 2] transforms it into [artifact 2], and [Module 3] generates [final output]. The arrows denote runtime information flow; the shaded boxes correspond to Sections X.Y-X.Z.`

## Annotated Overview Skeleton

```latex
\subsection{Overview}

% Role: task setting and tool purpose.
Given [input artifacts] from [SE task or ecosystem], [Tool] aims to help [developer/maintainer/tester/auditor/researcher] [perform action]. Unlike [simple baseline or current practice], [Tool] needs to account for [main design requirement] because [brief reason tied to the paper's challenge].

% Role: explicit input and output boundary.
[Tool] takes as input [input 1], [input 2], and optionally [input 3]. It produces [final output], which includes [output field 1], [output field 2], and [output field 3]. This output is designed to support [user decision or workflow action], rather than merely reporting [low-level signal].

% Role: complete tool figure and module map.
Figure X shows the overall workflow of [Tool]. The pipeline contains three modules. First, [Module 1] converts [raw input] into [intermediate artifact]. Second, [Module 2] analyzes [intermediate artifact] to produce [candidate result]. Third, [Module 3] validates, ranks, or explains the candidates and generates [final output].

% Role: subsection map. Make module names match figure labels.
Section X.1 describes [Module 1], including [main steps]. Section X.2 presents [Module 2], which [main operation]. Section X.3 explains [Module 3], which [final decision/reporting/action]. Section X.4 gives implementation details that apply across modules.

% Role: challenge or requirement mapping.
This design follows the challenges introduced in Section Y: [Module 1] addresses [C1/R1] by [short rationale], [Module 2] addresses [C2/R2] by [short rationale], and [Module 3] addresses [C3/R3] by [short rationale].
```

## More Concrete Example

```latex
\subsection{Overview}

Given a software project and a target maintenance task, \tool aims to produce an actionable report that identifies cases requiring developer attention. The tool takes project artifacts, execution evidence, and optional metadata as input. Its final output is a ranked set of findings, where each finding includes the affected artifact, the supporting evidence, and an explanation intended for developer inspection.

Figure~\ref{fig:overview} illustrates the workflow of \tool. The first module, Artifact Collection, gathers and normalizes project-level evidence into a unified case representation. The second module, Requirement-Aware Analysis, analyzes each case against the design requirements derived in Section~2. The third module, Evidence Validation and Reporting, filters unsupported candidates and generates the final ranked report.

The rest of this section follows the same order as the figure. Section~3.1 explains how \tool constructs the case representation from heterogeneous project artifacts. Section~3.2 describes how the analysis module derives candidate findings from this representation. Section~3.3 presents the validation and reporting module, which turns candidates into actionable outputs. Section~3.4 summarizes implementation details, including parser versions, model settings, thresholds, and runtime configuration.
```

## Reviewer Checks

1. Can a reviewer redraw the pipeline after reading the overview?
2. Are input artifacts and final output concrete enough to evaluate?
3. Do subsection titles match figure boxes?
4. Does the overview say more than the Introduction by naming intermediate artifacts and module relations?
5. Does the figure show information flow rather than only a list of components?