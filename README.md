# CRE Agent Skills - Research-Backed Commercial Real Estate Skill Library

**33 standalone AI skill files for U.S. commercial real estate analysis, plus 8 reusable knowledge bases, 11 industrial research notes, and 7 Claude Code plugins. Use them as Claude Code plugins, ChatGPT prompts, Cursor rules, or reference markdown in any LLM workflow.**

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/Skills-33-green.svg)](#skill-index)
[![Knowledge_Bases](https://img.shields.io/badge/Knowledge_Bases-8-blue.svg)](#knowledge-bases)
[![Research_Notes](https://img.shields.io/badge/Research_Notes-11-orange.svg)](#research-layer)
[![Claude_Code_Plugins](https://img.shields.io/badge/Claude_Code_Plugins-7-purple.svg)](#claude-code-plugins-recommended)

---

## What This Repo Is

`cre-agent-skills` is a markdown-first, open-source library of CRE analysis skills.

It now has three layers:

- **Multifamily Core**: the original acquisitions-focused multifamily skill set
- **Industrial v1**: a new U.S. industrial acquisitions pack, built with companion research notes
- **Shared CRE Workflows**: legal, closing, and document-ingestion tools that can support multiple sectors

This repo is designed so you can:

- copy a single skill into an LLM system prompt
- install a department or sector plugin into Claude Code
- point an AI agent at the repo and ask it to use the relevant skills
- inspect the research notes behind new sector-specific benchmarks and assumptions

> **No API keys. No compiled app. No orchestration required.** Every file is plain markdown or supporting documentation.

> **Disclaimer:** These skills are educational and operational aids, not financial, legal, investment, or tax advice. Use licensed counsel, brokers, lenders, engineers, and other professionals before making real-world decisions.

---

## Quick Start

### Option 1: Install a Claude Code Plugin

#### PowerShell

```powershell
git clone https://github.com/ahacker-1/cre-agent-skills.git
Set-Location .\cre-agent-skills

New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse .\claude-code-plugins\cre-industrial "$HOME\.claude\skills\"
```

Then in Claude Code:

```text
/cre-industrial Underwrite a 220,000 SF shallow-bay industrial acquisition in Atlanta
```

#### Bash

```bash
git clone https://github.com/ahacker-1/cre-agent-skills.git
cd cre-agent-skills

mkdir -p ~/.claude/skills
cp -r ./claude-code-plugins/cre-industrial ~/.claude/skills/
```

### Option 2: Copy a Single Skill File

Open any markdown file under `skills/`, copy it into your LLM tool, and load the related knowledge base if needed.

### Option 3: Point an AI Agent at the Repo

Clone the repo and tell your agent to use the relevant skill files and research notes for the deal at hand.

---

## Claude Code Plugins (Recommended)

Each plugin is a self-contained bundle with a `SKILL.md` entry point plus the referenced skills and knowledge files.

### Available Plugins

| Plugin | Slash Command | Scope |
|--------|---------------|-------|
| `cre-due-diligence` | `/cre-due-diligence` | Multifamily due diligence workflows |
| `cre-underwriting` | `/cre-underwriting` | Multifamily underwriting workflows |
| `cre-financing` | `/cre-financing` | Multifamily financing workflows |
| `cre-legal` | `/cre-legal` | Shared CRE legal workflows |
| `cre-closing` | `/cre-closing` | Shared CRE closing workflows |
| `cre-document-ingestion` | `/cre-document-ingestion` | Shared CRE document classification and parsing |
| `cre-industrial` | `/cre-industrial` | U.S. industrial acquisitions core workflows |

### Install All Plugins in PowerShell

```powershell
git clone https://github.com/ahacker-1/cre-agent-skills.git
Set-Location .\cre-agent-skills

New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse .\claude-code-plugins\* "$HOME\.claude\skills\"
```

### Project-Scoped Install in PowerShell

```powershell
New-Item -ItemType Directory -Force .\.claude\skills | Out-Null
Copy-Item -Recurse .\claude-code-plugins\cre-industrial .\.claude\skills\
```

### Use Without Copying

You can also reference a plugin directory directly:

```text
claude --add-dir /path/to/cre-agent-skills/claude-code-plugins/cre-industrial
```

---

## Skill Index

### Multifamily Core

These remain fully supported and keep their existing paths.

#### Due Diligence

- `skills/due-diligence/rent-roll-analyst.md`
- `skills/due-diligence/opex-analyst.md`
- `skills/due-diligence/market-study.md`
- `skills/due-diligence/physical-inspection.md`
- `skills/due-diligence/environmental-review.md`
- `skills/due-diligence/legal-title-review.md`
- `skills/due-diligence/tenant-credit.md`

#### Underwriting

- `skills/underwriting/financial-model-builder.md`
- `skills/underwriting/scenario-analyst.md`
- `skills/underwriting/ic-memo-writer.md`

#### Financing

- `skills/financing/lender-outreach.md`
- `skills/financing/quote-comparator.md`
- `skills/financing/term-sheet-builder.md`

### Shared CRE Workflows

These are broadly reusable across multiple sectors, though some still assume standard CRE acquisition workflows rather than every possible property type.

#### Legal

- `skills/legal/psa-reviewer.md`
- `skills/legal/title-survey-reviewer.md`
- `skills/legal/estoppel-tracker.md`
- `skills/legal/loan-doc-reviewer.md`
- `skills/legal/insurance-coordinator.md`
- `skills/legal/transfer-doc-preparer.md`

#### Closing

- `skills/closing/closing-coordinator.md`
- `skills/closing/funds-flow-manager.md`

#### Document Ingestion

- `skills/document-ingestion/document-classifier.md`
- `skills/document-ingestion/rent-roll-parser.md`
- `skills/document-ingestion/financials-parser.md`
- `skills/document-ingestion/offering-memo-parser.md`

### Industrial v1

These are new U.S.-only industrial acquisitions skills.

- `skills/industrial/industrial-market-study.md`
- `skills/industrial/industrial-lease-roster-analyst.md`
- `skills/industrial/industrial-lease-abstract-reviewer.md`
- `skills/industrial/industrial-tenant-credit-analyst.md`
- `skills/industrial/industrial-physical-inspection.md`
- `skills/industrial/industrial-underwriting-model-builder.md`
- `skills/industrial/industrial-financing-fit.md`
- `skills/industrial/industrial-ic-memo-writer.md`

---

## Knowledge Bases

### Multifamily Core Knowledge

- `knowledge/underwriting-calc.md`
- `knowledge/risk-scoring.md`
- `knowledge/multifamily-benchmarks.md`
- `knowledge/lender-criteria.md`
- `knowledge/legal-checklist.md`

### Industrial v1 Knowledge

- `knowledge/industrial-benchmarks.md`
- `knowledge/industrial-lease-structures.md`
- `knowledge/industrial-lender-criteria.md`

---

## Research Layer

Industrial v1 is the first sector pack in this repo built with required companion research notes.

Start here:

- [Research Standards](docs/RESEARCH-STANDARDS.md)
- [Industrial Research Index](research/industrial/INDEX.md)

Every industrial skill and knowledge base is supported by a companion note documenting:

- source table
- U.S.-only assumptions
- benchmark rationale
- conflicting-source resolution
- edge cases and red flags

---

## Common Workflows

### Multifamily Quick Underwrite

1. `rent-roll-analyst`
2. `opex-analyst`
3. `financial-model-builder`
4. `scenario-analyst`
5. `ic-memo-writer`

### Shared CRE Deal Intake

1. `document-classifier`
2. `financials-parser`
3. `offering-memo-parser`
4. relevant sector-specific diligence or underwriting skill

### Industrial v1 Acquisitions Core

1. `industrial-market-study`
2. `industrial-lease-roster-analyst`
3. `industrial-lease-abstract-reviewer`
4. `industrial-tenant-credit-analyst`
5. `industrial-physical-inspection`
6. `industrial-underwriting-model-builder`
7. `industrial-financing-fit`
8. `industrial-ic-memo-writer`

### Closing Readiness

1. `psa-reviewer`
2. `title-survey-reviewer`
3. `loan-doc-reviewer`
4. `insurance-coordinator`
5. `closing-coordinator`
6. `funds-flow-manager`

---

## Installation Methods

### Claude Projects

Upload the skill markdown file(s) you want plus any related knowledge base markdown files.

### ChatGPT or Custom GPTs

Paste the skill content into instructions and upload related knowledge bases as supporting files.

### Cursor / Windsurf / Other Editors

Store skill files as rules or reference them as prompt context.

### API Use

Read the skill file and related knowledge base into your system prompt.

---

## Project Structure

```text
cre-agent-skills/
├── skills/
│   ├── due-diligence/
│   ├── underwriting/
│   ├── financing/
│   ├── legal/
│   ├── closing/
│   ├── document-ingestion/
│   └── industrial/
├── knowledge/
│   ├── multifamily-benchmarks.md
│   ├── underwriting-calc.md
│   ├── lender-criteria.md
│   ├── legal-checklist.md
│   ├── risk-scoring.md
│   ├── industrial-benchmarks.md
│   ├── industrial-lease-structures.md
│   └── industrial-lender-criteria.md
├── research/
│   └── industrial/
├── claude-code-plugins/
│   ├── cre-due-diligence/
│   ├── cre-underwriting/
│   ├── cre-financing/
│   ├── cre-legal/
│   ├── cre-closing/
│   ├── cre-document-ingestion/
│   └── cre-industrial/
├── docs/
└── templates/
```

---

## Open-Source Contribution Standards

If you add new sector-specific skills:

- author root files under `skills/` or `knowledge/`
- create companion research notes under `research/`
- mirror plugin copies under `claude-code-plugins/`
- update docs and changelog in the same change

See:

- [Contributing](CONTRIBUTING.md)
- [Research Standards](docs/RESEARCH-STANDARDS.md)
- [Roadmap](docs/ROADMAP.md)

---

## FAQ

### Is this still a multifamily repo?

It started as a multifamily acquisitions library and still includes that full core set. It now also includes **Industrial v1** and is structured as a broader U.S. CRE skill library.

### Are the industrial skills global?

No. Industrial v1 is explicitly U.S.-only.

### Are the legacy shared skills fully sector-neutral?

Not completely. Legal, closing, and document-ingestion workflows are broadly reusable, but some legacy content still reflects acquisition-oriented CRE assumptions and some parsers still fit multifamily data best.

### Do I need all the files?

No. You can use a single skill file, a single plugin, or the full repo.

### Where do the industrial defaults come from?

Start with the [Industrial Research Index](research/industrial/INDEX.md). The industrial knowledge bases and skills were authored from those research notes.

---

## Want the Full Pipeline?

These skills were originally extracted from the [CRE Acquisition Orchestrator](https://github.com/ahacker-1/cre-acquisition-orchestrator), which models a larger multi-agent acquisition workflow. This repo is the lighter, markdown-first library version.

---

## Author

**Avi Hacker, J.D.** - AI Consulting for Commercial Real Estate

- [The AI Consulting Network](https://www.theaiconsultingnetwork.com)
- [AI Tactical Toolbox](https://avihacker.substack.com)
- [LinkedIn](https://linkedin.com/in/avi-hacker)

---

## License

[Apache 2.0](LICENSE)
