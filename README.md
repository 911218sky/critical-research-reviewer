# Critical Research Reviewer

A portable Markdown skill for rigorous, constructive evaluation of research claims, interpretations, study designs, and empirical conclusions.

## What it does

- Separates observations, evidence, assumptions, inferences, and speculation.
- Matches evidence to the exact population, intervention or exposure, comparator, outcome, and context.
- Identifies unsupported causal claims, confounding, selection effects, measurement problems, weak power, replication concerns, and boundary conditions.
- Presents the strongest credible counterargument rather than disagreeing for its own sake.
- Develops alternative explanations and concrete tests that can distinguish them.
- Reports sources transparently, including the source type and whether the material was checked in full text, an abstract, metadata, or a summary.
- Ends with a calibrated assessment and a useful next step.
- Supports a five-role panel: opposition, questioner, opportunity, outsider, and executor, followed by mutual examination and a chair's synthesis.

The skill never fabricates citations, results, tool calls, source access, or full-text verification. It does not force a literature search when the request is only a writing edit or does not require external evidence.

## Modes

`standard` is the default and preserves the single-reviewer workflow. Use `panel` or `five-role` when you want all five perspectives to debate the same problem and a chair to issue a final verdict. You can also request one role directly with `role:opposition`, `role:questioner`, `role:opportunity`, `role:outsider`, or `role:executor`.

Example request:

> 用 `panel` 模式審查這個方案：讓五個角色先獨立分析，再互相省察，最後由主席給出結論、停止條件，以及今天唯一要做的下一步。

Panel mode costs more reasoning and produces more output. It is most useful for consequential decisions, weak evidence, competing explanations, or a plan that may be based on an untested assumption. When the environment has no multi-agent runtime, the skill runs five isolated passes with the same model and reports that limitation; it must not claim that five independent AIs actually ran.

## Installation

Copy the skill directory into any Agent or assistant environment that supports Markdown-based skills. The runtime only needs to read `SKILL.md`; no package manager, plugin, language runtime, or platform-specific integration is required.

Example layout:

```text
skills/
└── critical-research-reviewer/
    ├── SKILL.md
    ├── README.md
    └── LICENSE
```

After installation, ask the assistant to critically review a claim, study design, interpretation, or literature summary. The skill defines a default response structure, but the user may request another format.

## Scope

This is a general-purpose review skill. It is not tied to a research field, project, operating system, model provider, Agent, editor, or command-line interface. When external research tools are available, the assistant should use the tools appropriate to the question and state what was actually examined. When they are unavailable, it should clearly limit the conclusion to the supplied material and established reasoning.

## License

GNU Affero General Public License v3.0 or later. See [`LICENSE`](LICENSE).
