# How to Use CRE Agent Skills

This guide covers how to use the repo as a broader U.S. CRE skills library, including the existing multifamily core, shared CRE workflows, and the new Industrial v1 pack.

---

## Claude Code

### Install a Plugin in PowerShell

```powershell
git clone https://github.com/ahacker-1/cre-agent-skills.git
Set-Location .\cre-agent-skills

New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse .\claude-code-plugins\cre-industrial "$HOME\.claude\skills\"
```

### Install a Plugin in Bash

```bash
git clone https://github.com/ahacker-1/cre-agent-skills.git
cd cre-agent-skills

mkdir -p ~/.claude/skills
cp -r ./claude-code-plugins/cre-industrial ~/.claude/skills/
```

### Use a Plugin

```text
/cre-industrial Review the lease roster and underwriting risks for a 180,000 SF shallow-bay asset in Dallas
```

### Use a Skill File Directly

Reference a root skill file in your prompt:

```text
Use the instructions in skills/industrial/industrial-market-study.md to evaluate this property.
```

---

## Claude Projects

Upload:

- one or more skill markdown files
- the related knowledge base markdown file(s)
- optionally, relevant research notes if you want the model to see the underlying source logic

Recommended starting combinations:

- Multifamily core: rent roll + OpEx + financial model + multifamily benchmarks
- Industrial v1: industrial market study + lease roster + underwriting + industrial knowledge bases

---

## ChatGPT / Custom GPTs

### Custom GPT

- Paste the skill content into the GPT instructions
- Upload the related knowledge bases as files
- Optionally upload research notes when you want source-traceable reasoning support

### Conversation-Level

- Paste the skill content as your first message
- Then provide the deal data and ask for the specific analysis

---

## Cursor / Windsurf / Other Editors

Use the files in one of two ways:

- as rules or context files in your project
- as reference markdown the assistant can read on demand

This works especially well when you want to combine a parser, a sector skill, and a knowledge base in one workflow.

---

## Any LLM or API Workflow

Load the root skill file into the system prompt and append the related knowledge base.

For new industrial workflows, the research note can be added as a third context layer when you want the model to see the benchmark rationale behind the prompt defaults.

---

## Recommended Skill Combinations

### Multifamily Acquisitions Core

- `rent-roll-analyst`
- `opex-analyst`
- `financial-model-builder`
- `scenario-analyst`
- `ic-memo-writer`

### Shared CRE Deal Intake

- `document-classifier`
- `financials-parser`
- `offering-memo-parser`

### Industrial v1 Acquisitions Core

- `industrial-market-study`
- `industrial-lease-roster-analyst`
- `industrial-lease-abstract-reviewer`
- `industrial-tenant-credit-analyst`
- `industrial-physical-inspection`
- `industrial-underwriting-model-builder`
- `industrial-financing-fit`
- `industrial-ic-memo-writer`

### Closing Readiness

- `psa-reviewer`
- `title-survey-reviewer`
- `insurance-coordinator`
- `loan-doc-reviewer`
- `closing-coordinator`
- `funds-flow-manager`

---

## Tips for Best Results

1. Provide the property subtype whenever possible.
2. For industrial deals, include clear height, loading, trailer parking, office finish, and power if you have them.
3. Keep lease data separate from market assumptions. The industrial skills work best when the current lease story and the market story are both visible.
4. Use the knowledge bases for reusable context and the research notes when you want source-backed traceability.
5. Treat time-sensitive rent, spread, and lender assumptions as directional. Validate current local market conditions before acting on them.
