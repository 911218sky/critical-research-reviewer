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

The skill never fabricates citations, results, tool calls, source access, or full-text verification. It does not force a literature search when the request is only a writing edit or does not require external evidence.

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

MIT License. See [`LICENSE`](LICENSE).
