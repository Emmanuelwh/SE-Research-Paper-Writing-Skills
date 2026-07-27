# Evaluation Examples

Use this file as the entry point for Evaluation examples. Read `references/evaluation.md` first, then open only the example that matches the current writing task.

## Tool Paper Examples

1. RQ design for Tool Papers: `references/examples/evaluation/rq-design-tool-paper.md`
2. Experimental setup: `references/examples/evaluation/experimental-setup-example.md`
3. RQ result presentation and analysis: `references/examples/evaluation/rq-result-analysis-example.md`

## RQ Design Mini-Pattern

`We aim to address the following research questions: RQ1 asks [main effectiveness]. RQ2 compares [Tool] with [existing methods/current practice]. RQ3 evaluates whether [modules/design choices] are necessary. RQ4 examines whether [Tool] works on [real-world subjects/settings].`

## Experimental Setup Mini-Pattern

`We constructed the dataset from [source] using [criteria]. The final dataset contains [scale] and covers [diversity]. We use [metrics] because they measure [constructs]. We compare against [baselines] under the same [protocol]. We implemented [Tool] in [language/framework] and ran experiments on [environment].`

## RQ Result Paragraph

`RQ[x]: [short answer]. Table/Figure [n] shows [main evidence]. Specifically, [concrete result]. The result occurs because [module/design/baseline behavior/dataset property]. However, [boundary/failure case]. Therefore, [bounded answer].`

## Baseline Justification

`We compare against [baseline] because it represents [current practice/recent research/simple heuristic]. This comparison tests whether [proposed method] improves over a realistic alternative rather than only over a weak reference point.`

## Ablation Paragraph

`Removing [module/design choice] reduces [metric] from [value] to [value], indicating that [module/design choice] contributes to [capability]. This supports the design claim in Section [x] that [reason].`

## Real-World Evaluation Paragraph

`On [real-world subjects], [Tool] reported [number] candidates. Manual validation confirmed [number] true [bugs/vulnerabilities/issues]. [Number] were [reported/acknowledged/patched]. These results suggest [practical value], while [unconfirmed/false-positive cases] show [boundary].`

## Failure Case Paragraph

`The main failure cases occur when [condition]. Manual inspection shows that [reason]. These failures indicate that [method/tool] is less reliable for [scope], which bounds our claim about [claim].`

## Practical Implication Paragraph

`For practitioners, this result means that [actionable implication]. For researchers, it suggests that future work should [research implication]. We therefore interpret the improvement as [bounded claim], not as evidence that [overclaim].`