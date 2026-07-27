# Methodology Writing Guide

## Goal

Write Methodology so reviewers can understand the complete design before evaluating details. For SE Tool Papers, Methodology should explain the tool as an engineered workflow: what task it supports, what inputs it consumes, what outputs it produces, how modules transform artifacts step by step, and why each design choice is necessary for the paper's stated challenges.

Do not write Methodology as a loose implementation diary. Do not only repeat the Abstract or Introduction. Compared with those sections, Methodology can be more concrete about modules, data structures, algorithms, prompts, rules, runtime steps, manual procedures, and implementation boundaries.

## Pre-Writing Inventory

Before drafting, answer these questions in a table:

1. What is the tool's user-facing task?
2. What are the exact inputs: source code, tests, traces, logs, issues, commits, transactions, prompts, documentation, configurations, user reports, or benchmark tasks?
3. What is the final output: warning, ranked list, patch, test, explanation, report, label, trace, dataset, recommendation, or workflow action?
4. What intermediate artifacts does the tool produce?
5. What modules transform one artifact into the next?
6. Which challenge, design requirement, or RQ motivates each module?
7. What implementation details are needed for reproducibility but not better placed in Evaluation?

Useful planning table:

| Module | Input | Main Operation | Output | Why Needed | Feeds Into |
| --- | --- | --- | --- | --- | --- |
| [M1] | [artifact/evidence] | [transformation] | [intermediate artifact] | [challenge/requirement] | [M2] |
| [M2] | [M1 output] | [analysis/reasoning/ranking/generation] | [intermediate artifact] | [challenge/requirement] | [M3] |
| [M3] | [M2 output] | [decision/validation/reporting] | [final output] | [actionability/trust] | [user/evaluation] |

## Part 1: Opening Overview for a Tool Paper

The first Methodology subsection should be an overview of the whole tool. Its job is to let reviewers understand the system diagram before reading module details.

### Required Content

The overview must answer:

1. What problem setting and user task does the tool address?
2. What are the tool's inputs and final outputs?
3. What are the main modules or stages?
4. What intermediate representation, artifact, or state passes between modules?
5. Which later subsection explains each module?
6. Which challenge or design requirement from the Introduction motivates each module?
7. Where does the complete tool figure appear, and what should readers learn from it?

### Recommended Paragraph Order

1. Task and tool purpose: state the SE task, the actor, and the action the tool supports.
2. Input and output: specify the input boundary and final output boundary.
3. Pipeline figure: point to Figure X and name the major modules in execution order.
4. Section map: explain what each Methodology subsection covers and how its output feeds the next one.
5. Requirement map: briefly connect major modules to the challenges or design requirements introduced earlier.

### Complete Tool Figure

Include a complete tool figure when the method has more than one module. The figure should show the tool as a pipeline or workflow, not as decorative architecture.

The figure should include:

1. Input artifacts at the left boundary.
2. Final output at the right boundary.
3. Major modules as named boxes matching subsection titles.
4. Intermediate artifacts on arrows or between modules.
5. Optional external resources such as models, rules, corpora, APIs, or human feedback.
6. Optional failure handling, filtering, validation, or ranking steps when they are central to the design.

The caption should state the argument of the figure: how information flows through the tool and why the modules are ordered this way.

Avoid:

1. Showing every implementation class, script, or UI widget.
2. Using names in the figure that do not match subsection titles.
3. Hiding inputs or final outputs.
4. Putting evaluation metrics in the overview figure unless they are part of the tool's runtime output.
5. Making the figure imply capabilities that Methodology never explains.

Example reference:

- `references/examples/methodology/tool-overview-example.md`

## Part 2: Writing Module Subsections

After the overview, introduce each module in the order shown in the tool figure. A module subsection should make three things explicit: what the module does, why the module is needed, and why the design is appropriate for the SE task.

### Module Lead Paragraph

Start each module with one bridging paragraph before detailed subsections. The paragraph should:

1. Briefly state what the previous module or input has produced.
2. State the next problem, uncertainty, or design requirement.
3. Explain why a naive or existing approach is insufficient when useful.
4. Use `To address this...`, `To overcome this...`, or equivalent logic to introduce the module.
5. Preview the module's output and how it will be used later.

Lead paragraph skeleton:

`The previous stage produces [intermediate artifact]. However, [remaining problem] prevents the tool from [desired capability]. To address this, [Tool] performs [module action], which [main design idea]. This module outputs [artifact], which is used by [next module/subsection] to [next purpose].`

### Subsection Structure Inside a Module

Use subsubsections or paragraphs only when the module has meaningful internal technical units. Do not force every module into a fixed three-step pattern. The structure should follow the real execution logic of the tool: what artifact enters the module, what local problem must be solved, what technical operations transform the artifact, and what artifact leaves the module.

Recommended structure:

1. Local objective and input: define what this module receives and what it must produce for the next module.
2. Execution flow: describe the operations in the order they run, using as many or as few technical units as the module actually needs.
3. Local obstacle and design response: when a difficulty appears inside the process, explain it with `To address/overcome this...` and introduce the corresponding design choice.
4. Technical detail: give the algorithm, rule, representation, prompt, parser, data structure, constraint, or implementation procedure needed to understand the operation.
5. Intermediate and final outputs: name the artifacts produced after important operations and explain how they are consumed later.
6. Reproducibility details: include settings, thresholds, model versions, schemas, prompt formats, fallback behavior, or runtime constraints only when they affect the method.

Technical-unit sentence patterns:

1. `Given [module input], this unit [operation] and produces [intermediate output].`
2. `During this process, [specific difficulty] arises because [reason]. To address this, we [design choice].`
3. `Concretely, we [implementation detail 1], [implementation detail 2], and [implementation detail 3].`
4. `The output is [artifact/state], which provides [information/capability] for [next unit/module].`

### Why and How Balance

A strong SE Methodology does not stop at implementation details. For each important step, explain why the design is appropriate for the target SE task.

Good reasons include:

1. It preserves a relation that current tools lose.
2. It reduces manual effort or reviewer-visible ambiguity.
3. It makes outputs actionable for developers, auditors, maintainers, or researchers.
4. It improves reproducibility by making labels, prompts, rules, or thresholds explicit.
5. It supports later evaluation by producing measurable intermediate or final artifacts.
6. It handles realistic ecosystem constraints such as noisy logs, incomplete metadata, changing dependencies, flaky tests, or heterogeneous project structure.

Avoid vague advantages such as `effective`, `robust`, `comprehensive`, or `practical` unless Methodology defines what the word means and Evaluation measures it.

### Module Ending

End each module by stating:

1. What artifact the module outputs.
2. What assumption or limitation remains.
3. Which later module or evaluation question uses the output.

Example reference:

- `references/examples/methodology/module-subsection-example.md`

## Tool Paper Structure

Use this structure when the paper's main contribution is a tool, system, analyzer, detector, repair method, testing technique, auditing framework, benchmarked workflow, or LLM4SE pipeline.

1. Overview: full workflow, complete tool figure, inputs, outputs, module map, and challenge mapping.
2. Problem formulation or design goals: include only if formal definitions or requirements are needed before modules.
3. Module 1: motivation, input, operation, output, and addressed challenge.
4. Module 2: motivation, input, operation, output, and addressed challenge.
5. Module 3: integration, validation, ranking, repair, reporting, or user-facing output.
6. Implementation details: include reproducibility details that cut across modules.

## Empirical Study Structure

Use this structure when the main contribution is an empirical study rather than a tool.

1. Study overview: RQs, data sources, and analysis pipeline.
2. Data collection: sources, time window, sampling, inclusion/exclusion criteria.
3. Data preprocessing: cleaning, filtering, deduplication, normalization, labeling.
4. Measurement or operationalization: variables, constructs, metrics, coding scheme.
5. Analysis method: statistical analysis, qualitative coding, manual inspection, case study, or mixed methods.
6. Reproducibility: artifacts, scripts, annotation protocol, prompts, and replication package.

## Component Writing Pattern

For each component or study phase, write:

1. Motivation: why this component is needed for the paper's challenge, RQ, or design goal.
2. Input: what data, artifact, state, or evidence it receives.
3. Design: how it works in execution order.
4. Output: what it produces.
5. Link: how the output feeds the next component or answers an RQ.
6. Advantage: why this design is appropriate compared with simpler alternatives.
7. Boundary: what the module does not guarantee, when relevant.

## Checklist

1. Does Methodology begin with a full tool overview and complete figure when appropriate?
2. Are the tool's inputs and final outputs explicit?
3. Do module names in the figure match subsection titles?
4. Does every challenge or design requirement from the Introduction map to a module or study-design element?
5. Does each module start with a lead paragraph that explains previous output, remaining problem, proposed module, and next output?
6. Does each step explain why it is needed, how it works, and what it produces?
7. Are implementation details concrete enough for reproducibility?
8. Are evaluation results kept out of Methodology except when describing runtime outputs or design choices?
9. Are assumptions and boundaries clear enough to prevent overclaiming?
10. Are terms consistent across Overview, module subsections, Evaluation, and figures?