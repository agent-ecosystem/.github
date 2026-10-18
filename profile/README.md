# Agent Ecosystem Collective

Independent research on how AI coding agents interact with documentation, tools, and web
infrastructure. We publish what we measure: open specifications, empirical reports, and the
tooling that makes compliance testable.

The collective is self-funded and has no commercial stake in any platform or vendor.

**[agentecosystem.dev](https://agentecosystem.dev)**

## Specifications

**[Agent-Friendly Documentation Spec](https://agentdocsspec.com)** (draft v0.6.0). 28 checks
across 7 categories that evaluate how well a documentation site serves agent consumers:
discovery, markdown availability, page size and truncation risk, content structure, URL
stability, observability, and authentication. Each check has defined pass/warn/fail criteria,
an automation level, and a severity.
[Repository](https://github.com/agent-ecosystem/agent-docs-spec)

## Tools

| Tool | What it does |
| --- | --- |
| [afdocs](https://afdocs.dev) | Audits any documentation site against all 28 checks of the spec. Powers [Agent Score](https://buildwithfern.com/agent-score) by Fern. Try it: `npx afdocs check <url>` |
| [skill-validator](https://github.com/agent-ecosystem/skill-validator) | Validates and scores [Agent Skills](https://agentskills.io): spec compliance, link resolution, token counts, content quality metrics, and LLM-as-judge scoring |
| [agentsummons](https://agentsummons.dev) | Invokes agent harnesses headlessly behind one API and one CLI: Antigravity CLI, Claude Code, Codex CLI, and GitHub Copilot CLI |
| [agentminutes](https://agentminutes.dev) | Parses those harnesses' native session logs into one unified, comparable event schema |
| [skillxp](https://skillxp.dev) | Stages a skill on a real harness and reports what actually reached the model, with transcript evidence instead of model self-reporting |
| [agent-traffic-classifier](https://github.com/agent-ecosystem/agent-traffic-classifier) | Classifies server log traffic into twelve categories, from coding agents and AI crawlers to vulnerability scanners |
| [topicsleuth](https://github.com/agent-ecosystem/topicsleuth) | Detects and tracks topic activity from a stream of documents. |

## Benchmarks and reports

| Output | What it covers |
| --- | --- |
| [Agent Skill Implementation](https://agentskillimplementation.com) | How agent platforms actually load, manage, and present Agent Skills. 46 checks across 10 categories, 44 of them automated, with published reports for four harnesses |
| [Agent Reading Test](https://agentreadingtest.com) | Ten task pages that measure what a coding agent really retrieves from a web page, using embedded canary tokens and scored out of 20 points |
| [Agent Skill Report](https://agentskillreport.com) | Qualitative analysis of 673+ public Agent Skills, including spec compliance findings across the ecosystem |

## Where to start

- **Documentation teams**: run `npx afdocs check <your-docs-url>`, then work through
  [Improve Your Score](https://afdocs.dev/improve-your-score).
- **Skill authors**: run skill-validator over your skill, then read the
  [platform reports](https://agentskillimplementation.com) for how harnesses diverge from each
  other and from the spec.
- **Docs platform builders**: the [spec](https://agentdocsspec.com) and the platform
  findings are the shortest route to what agents need from the surfaces you own.

Commentary on ecosystem developments is published at [aeshift.com](https://aeshift.com).

Everything in this organization is open source. Individual support is possible through
[GitHub Sponsors](https://github.com/sponsors/dacharyc).
