# Skills: SE Research Paper Writing

[中文介绍](./README_zh.md).

> Important Attribution and Adaptation Notice
>
> This repository is adapted from the original `research-paper-writing` skill structure and writing workflow.
> https://github.com/Master-cai/Research-Paper-Writing-Skills
> The original writing knowledge and methodology were largely inspired by Prof. Peng Sida's open study notes:
> https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e
>
> Prof. Peng's original repository:
> https://github.com/pengsida/learning_research
>
> This repository keeps the reusable Skill packaging idea, section-oriented guidance, paragraph-flow checks,
> claim-evidence alignment, and reviewer-facing self-review workflow, then adapts them for software engineering
> research papers and top SE venues.
>
> Compared with the original general research-paper writing skill, this version reorganizes the content around
> software engineering paper conventions: research questions, methodology transparency, empirical/software-artifact
> evidence, evaluation design, threats to validity, reproducibility, and SE reviewer expectations.

This repository provides one Codex-compatible skill package for software engineering research paper writing:

- `se-research-paper-writing/`
  - `SKILL.md`: core workflow, usage rules, and output contract
  - `references/`: section-specific writing guides for SE papers
  - `agents/openai.yaml`: UI metadata

## Intended Users

Use this skill when preparing papers for software engineering conferences and journals such as ICSE, FSE, ASE, ISSTA, MSR, SANER, ICSME, TSE, TOSEM, EMSE, and JSS.

## Typical Use Cases

- Drafting or rewriting Abstract, Introduction, Related Work, Methodology, Evaluation, and Threats to Validity
- Designing research questions and contribution-evidence maps
- Checking whether claims are supported by experiments, empirical data, user studies, or case studies
- Reviewing a paper from a skeptical SE reviewer perspective before submission
- Improving paragraph flow, terminology consistency, and reviewer-facing presentation

## Installation

Assume you are in the repository root.

### Codex

Copy the skill into `$CODEX_HOME/skills/`:

```bash
mkdir -p "$CODEX_HOME/skills"
cp -R se-research-paper-writing "$CODEX_HOME/skills/"
```

Usage example:

```text
Use $se-research-paper-writing to improve my ICSE paper introduction.
```

### Claude Code

Global:

```bash
mkdir -p "$HOME/.claude/skills"
cp -R se-research-paper-writing "$HOME/.claude/skills/"
```

Project-level:

```bash
mkdir -p .claude/skills
cp -R se-research-paper-writing .claude/skills/
```

### Gemini

```bash
mkdir -p "$HOME/.gemini/skills"
cp -R se-research-paper-writing "$HOME/.gemini/skills/"
```

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).
