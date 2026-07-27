# RQ Result and Analysis Example

Use this example when writing each RQ subsection after Experimental Setup.

## RQ Subsection Skeleton

```latex
\subsection{RQ1: [Question]}

% Short answer first.
[Tool] [main answer], achieving [key result] on [dataset/setting].

% Table or figure orientation.
Table~\ref{tab:rq1} reports [metrics] for [methods] on [datasets/settings]. The table compares [Tool] with [baselines] under the same [protocol].

% Detailed result.
[Tool] achieves [number] in [metric], outperforming [baseline] by [difference]. The gain is consistent on [settings] but smaller on [hard setting].

% Cause analysis.
The improvement mainly comes from [module/design choice], which [mechanism]. In contrast, [baseline] relies on [assumption], causing [failure mode] when [condition].

% Boundary.
The remaining errors occur when [condition]. These cases suggest that [Tool] is less reliable for [scope], which bounds our claim to [bounded setting].

% Takeaway.
Answer to RQ1: [one-sentence bounded answer].
```

## Effectiveness Result Pattern

`Table X shows that [Tool] achieves [metric values] on [dataset]. Compared with [baseline/SOTA], [Tool] improves [metric] by [delta]. This suggests that [Tool] is effective for [task]. The improvement is mainly due to [module/design], which [reason]. Performance is weaker on [case type], because [reason].`

## Ablation Result Pattern

`Table X compares the full [Tool] with variants that remove or replace [modules]. Removing [module] reduces [metric] from [value] to [value], showing that [module] is necessary for [capability]. Replacing [design choice] with [simpler alternative] causes [effect], indicating that [design choice] helps [reason].`

## Real-World Result Pattern

`On [real-world subjects], [Tool] reported [number] candidates. Manual validation confirmed [number] true [bugs/vulnerabilities/issues], including [severity/status]. [Number] findings were [reported/acknowledged/patched] by developers. These results show that [Tool] can produce actionable findings in real settings. The unconfirmed cases mainly involve [reason], which suggests [boundary].`

## SOTA Comparison Analysis Pattern

`[Baseline] performs well on [case type] because [reason]. However, it misses [case type] because [missing capability/assumption]. [Tool] handles these cases by [module/design]. This explains why [Tool] improves [metric] while [baseline] remains competitive on [scope].`

## Table Caption Patterns

1. `Performance of [Tool] and baselines on [dataset]. Higher [metric] and lower [metric] are better.`
2. `Ablation study of [Tool]. Each variant removes or replaces one design choice from the full tool.`
3. `Real-world findings reported by [Tool], grouped by [project/ecosystem/status/severity].`
4. `Runtime and resource usage of [Tool] across [project sizes/input sizes/settings].`

## Common Fixes

1. If a result subsection starts with a table, add a short-answer sentence before the table.
2. If the analysis only says `our method performs better`, explain the mechanism.
3. If baseline comparison is one-sided, state where baselines work well.
4. If real-world results are only candidate counts, add confirmation protocol or avoid strong impact claims.
5. If an ablation table includes arbitrary variants, tie each variant to a Methodology module or design claim.