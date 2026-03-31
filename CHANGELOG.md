# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

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
