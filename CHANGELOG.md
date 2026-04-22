# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.2.0] - 2026-04-22

### Added

- Brokerage Investment Sales v1 release with 8 new U.S.-focused seller-side brokerage skills
  - assignment intake manager
  - broker opinion of value builder
  - listing proposal builder
  - offering memorandum and teaser writer
  - buyer process and data room manager
  - call for offers and bid leveling analyst
  - deal term negotiation brief builder
  - PSA to close transaction coordinator
- 4 brokerage knowledge bases
  - brokerage investment sales process
  - broker opinion of value guidance
  - marketing confidentiality and buyer process
  - offer negotiation and closing playbook
- 12 brokerage companion research notes under `research/brokerage/`
- New Claude Code plugin: `cre-brokerage`
- New documentation:
  - `docs/releases/brokerage-v1.md`
  - `docs/releases/brokerage-v1-pr-summary.md`

### Changed

- Updated the public docs to position Brokerage Investment Sales v1 as an additive `v1.2.0` release on top of the original multifamily-first repo and the prior Industrial v1 release
- Extended usage and skill-index docs with role-based brokerage workflows
- Updated contributing guidance so role-based packs follow the same research-backed standard as sector packs

## [1.1.0] - 2026-04-22

### Added

- Industrial v1 sector expansion with 8 new U.S.-focused industrial acquisition skills
  - industrial market study
  - industrial lease roster analysis
  - industrial lease abstract review
  - industrial tenant credit analysis
  - industrial physical inspection
  - industrial underwriting model builder
  - industrial financing fit
  - industrial IC memo writer
- 3 industrial knowledge bases
  - industrial benchmarks
  - industrial lease structures
  - industrial lender criteria
- 11 industrial companion research notes under `research/industrial/`
- New Claude Code plugin: `cre-industrial`
- New documentation:
  - `docs/RESEARCH-STANDARDS.md`
  - `docs/ROADMAP.md`
  - `docs/releases/industrial-v1.md`
  - `docs/releases/industrial-v1-pr-summary.md`

### Changed

- Repositioned the repo as a broader U.S. CRE skill library spanning multifamily core, shared CRE workflows, and industrial v1
- Updated `README.md`, `docs/HOW-TO-USE.md`, and `docs/SKILL-INDEX.md` to reflect the new sector structure
- Updated `CONTRIBUTING.md` to require companion research notes for new sector content
- Added PowerShell plugin installation examples alongside existing Claude Code usage guidance
- Lightly broadened shared document-ingestion wording so intake workflows read cleanly for industrial and broader CRE use cases

## [1.0.0] - 2026-03-30

### Added

- 25 standalone CRE analysis skills extracted from [CRE Acquisition Orchestrator](https://github.com/ahacker-1/cre-acquisition-orchestrator)
  - 7 Due Diligence skills (rent roll, OpEx, market, physical, environmental, title, tenant credit)
  - 3 Underwriting skills (financial model, scenario analysis, IC memo)
  - 3 Financing skills (lender outreach, quote comparison, term sheet)
  - 6 Legal skills (PSA, title/survey, estoppels, loan docs, insurance, transfer docs)
  - 2 Closing skills (closing coordinator, funds flow)
  - 4 Document Ingestion skills (classifier, rent roll parser, financials parser, OM parser)
- 5 domain knowledge bases (underwriting calculations, risk scoring, multifamily benchmarks, lender criteria, legal checklist)
- 6 Claude Code plugins — one per department with SKILL.md entry points and bundled knowledge bases
- Sample input templates (rent roll CSV, T-12 CSV, deal summary template)
- Full documentation (README, HOW-TO-USE guide, SKILL-INDEX quick reference)
