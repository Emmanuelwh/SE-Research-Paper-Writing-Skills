# Tool Paper Module Subsection Example

Use this example when writing a module after the Methodology overview. A module subsection should follow the real technical process, not a fixed number of steps. The key is to make the local input, local problem, technical operations, intermediate artifacts, and final output explicit.

## Module Subsection Shape

```latex
\subsection{[Module Name]}

% Lead paragraph: previous output/input -> remaining local problem -> proposed module -> module output.
[Previous module or raw input] provides [artifact/state/evidence]. However, [local problem] makes it difficult to [capability needed by the tool]. To address this, [Tool] performs [module-level operation], which [high-level design idea]. The module outputs [artifact/state], which is used by [next module or final tool output] to [next purpose].

% Technical unit 1: use a paragraph or subsubsection only if it is a meaningful operation.
\subsubsection{[Technical Unit Name]}
Given [input to this unit], [Tool] [operation] to produce [intermediate artifact]. This operation is needed because [why this transformation is necessary for the module]. Concretely, [Tool] [implementation detail 1], [implementation detail 2], and [implementation detail 3]. The resulting [artifact] records [important information] and becomes the input to [next unit/module].

% Technical unit 2: introduce a local obstacle only when the process has one.
\subsubsection{[Technical Unit Name]}
During [operation/process], [specific difficulty] arises because [reason]. To address this, [Tool] [design choice]. This design [preserves/reduces/aligns/derives/constructs] [needed property] while avoiding [failure mode or unnecessary cost]. The unit outputs [artifact/state], which [next unit/module] uses to [purpose].

% Output paragraph: close the module by naming its product and boundary.
The final output of [Module Name] is [module output]. It contains [fields/properties] and is passed to [next module]. This module does not yet [remaining task], which is handled by [later module/subsection].
```

## Technical Unit Checklist

For each technical unit, answer only the questions that matter for the actual process:

1. What artifact or state enters this unit?
2. What transformation, analysis, generation, construction, or measurement is performed?
3. Why is this operation necessary at this point in the pipeline?
4. What difficulty appears during the operation, if any?
5. What design choice addresses that difficulty?
6. What intermediate artifact is produced?
7. What later unit or module consumes that artifact?

## Generic Example with Annotations

```latex
\subsection{Candidate Construction}

% Lead paragraph.
The previous module converts raw project artifacts into a normalized evidence representation. However, the tool still needs to turn this representation into concrete candidates that can be inspected or processed later. A direct enumeration of all possible candidates would include many irrelevant cases and would make the later analysis expensive. To address this, \tool constructs candidates by combining evidence selection with task-specific constraints. The module outputs candidate records, which are consumed by the next module to derive the final tool output.

\subsubsection{Evidence Selection}

% Input -> operation -> output.
Given the normalized evidence representation, \tool first selects the evidence relevant to the target task. This operation is necessary because the normalized representation may contain information that is useful for traceability but irrelevant to candidate construction. Concretely, \tool identifies the artifact types required by the task, extracts the fields used by later reasoning, and preserves provenance links for each selected item. The output is a task-specific evidence set that records both the selected content and its source.

\subsubsection{Candidate Formation}

% Local obstacle -> design response -> output.
During candidate formation, the main difficulty is that relevant evidence may be incomplete, redundant, or expressed at different granularities. To address this, \tool constructs candidates around a stable unit of analysis, such as an artifact, event, entity, interaction, or workflow instance. For each unit, \tool groups the selected evidence, removes duplicate support, and records missing fields explicitly instead of silently discarding the candidate. This design keeps the candidate inspectable while allowing later modules to decide whether the evidence is sufficient.

\subsubsection{Candidate Representation}

% Technical detail and module output.
Each candidate is represented as a record with [field 1], [field 2], [field 3], and provenance links. [Field 1] identifies the unit being analyzed; [field 2] stores the evidence used to construct the candidate; [field 3] stores the local status needed by the next module. The final output of this module is a set of candidate records. These records are passed to Section~X.Y, which [analyzes/refines/explains/uses] them to produce [next artifact or final output].
```

## Common Fixes

1. If the subsection assumes a fixed step count, restructure it around the module's real technical units.
2. If the subsection only lists operations, add the local input, local problem, and output connection.
3. If a paragraph says `we use X`, add what problem X solves in this specific process.
4. If a process difficulty appears, use `To address this...` to introduce the design response.
5. If an output is vague, name the artifact fields or properties consumed later.
6. If details feel like Evaluation, keep only runtime behavior, representations, settings, or design rationale.