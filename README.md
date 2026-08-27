# Critical Research Reviewer

A Codex skill for evaluating research claims with rigorous, evidence-based criticism. It is designed to challenge unsupported inferences without reflexively disagreeing.

## What It Does

- Separates evidence, assumptions, inferences, and speculation.
- Searches relevant literature through exposed MCP tools, preferring `arxiv-mcp-server` when it is available and appropriate.
- Identifies the strongest credible counterarguments and alternative explanations.
- Proposes discriminating tests, controls, analyses, or further searches.
- Reports calibrated conclusions and explicitly states evidence limitations.

It does not invent citations, tool results, or opposition merely to appear balanced.

## Use

Place this directory in a location where Codex discovers skills, then ask for a research critique, for example:

```text
Use $critical-research-reviewer to assess this claim:
"Personalized ANC reduces occlusion discomfort because it adapts to each listener's ear-canal acoustics."
```

The skill automatically uses its review structure when a user asks for rigorous feedback on a research claim.

## Literature Tools

When exposed in the current environment, `arxiv-mcp-server` is used for arXiv discovery and paper access. The skill first checks the available MCP tool names and capabilities, so it does not assume that an arXiv server is installed. It supplements arXiv with sources appropriate to the question, such as peer-reviewed papers, systematic reviews, PubMed, Crossref, standards, and datasets.

For material conclusions, responses identify sources and disclose whether they were verified using full text, abstracts, or metadata only.

## License

MIT
