# Research Standards for New Sector Skills

This repository now uses a research-backed authoring standard for all **new** sector packs, knowledge bases, and complex skills. The goal is to keep prompts concise while making the supporting benchmarks, assumptions, and source logic transparent for contributors and users.

## Scope

Use this standard whenever you add or materially expand:

- A new skill under `skills/`
- A new knowledge base under `knowledge/`
- A new Claude Code plugin sector bundle under `claude-code-plugins/`
- A new sector pack such as industrial, office, retail, self-storage, or future multifamily depth modules

Existing multifamily files do not need to be retrofitted all at once, but future updates should move toward this standard when practical.

## Source of Truth

- `skills/` and `knowledge/` are the root authored files.
- `claude-code-plugins/` contains mirrored distribution copies for Claude Code.
- `research/` contains the supporting research notes that justify new benchmarks, formulas, thresholds, and sector-specific defaults.

## Required Companion Research

Every new skill or knowledge base must have a companion research note before it is merged.

Minimum requirements:

- One markdown research note per new skill or knowledge base
- At least 10 cited sources
- At least 3 primary or quasi-primary sources when available
- Explicit U.S.-only vs broader-market assumptions
- Publish date and access date for time-sensitive sources
- Clear benchmark or formula rationale for anything that becomes a default in the repo

## Recommended Source Hierarchy

Use the strongest available sources first:

1. Primary and quasi-primary sources
   - Government and regulatory agencies
   - Public company filings
   - Lender program materials
   - Official standards bodies
   - Market participants publishing their own lending or operating criteria
2. Institutional market research
   - CBRE
   - JLL
   - Cushman & Wakefield
   - NAIOP
   - SIOR
   - Prologis and other public REIT research
   - MBA, CREFC, Trepp, MSCI, or similar sector data providers
3. Practitioner and legal commentary
   - National law firms
   - Technical advisors
   - Industry explainers used for issue spotting, not hard-coded rules

Avoid anonymous blogs, forum posts, or uncited benchmark lists as support for default thresholds.

## Required Research Note Template

Use the following structure for each new research note.

```markdown
# [Topic]

## Purpose
- What file(s) this research supports
- Who the intended user is

## U.S.-Only Assumptions
- Geography
- Deal type
- Legal and market assumptions

## Source Table
| Source | Publisher | URL | Publish Date | Access Date | Source Type | Notes |
|--------|-----------|-----|--------------|-------------|-------------|-------|

## Key Findings
- Short synthesized findings grouped by topic

## Benchmark and Formula Decisions
- Which benchmarks are suitable as repo defaults
- Which benchmarks should remain case-by-case only
- Any formulas, ranges, or directional guidance derived from the research

## Conflicting Source Resolution
- Where sources disagreed
- Which source type took priority and why

## Edge Cases and Red Flags
- Cases where the skill should avoid hard-coded defaults
- Situations that require local counsel, lender feedback, or market-specific overrides

## Open Questions
- Known research gaps or topics intentionally deferred
```

## Skill Authoring Rules

When converting research into a new skill:

- Keep the skill clean and practical; do not turn it into a bibliography
- Add a short `Research Basis` section near the end that points to the relevant research note
- Use only traceable defaults
- Label time-sensitive market data as directional, not universal
- Prefer subtype-aware guidance over one-size-fits-all industrial or sector assumptions

## Knowledge Base Authoring Rules

Knowledge bases should:

- Distill the research into reusable reference material
- Include a `Last updated` date
- State scope limitations
- Tell users to validate current local market conditions where rates, spreads, or leasing conditions are time-sensitive

## Merge Expectations

Before merging a new sector pack:

- Companion research notes exist for each new skill and knowledge base
- Root files under `skills/` and `knowledge/` are complete
- Plugin mirrors are updated in the same change
- Docs explain where the new sector fits in the repo
- Changelog and release notes are updated if the change is public-facing
