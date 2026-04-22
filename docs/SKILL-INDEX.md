# Skill Index — Quick Reference

Find the right skill for your task. Each entry shows what the skill does, what inputs it needs, and which knowledge bases to pair it with.

---

## Due Diligence

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [Rent Roll Analyst](../skills/due-diligence/rent-roll-analyst.md) | Validate revenue quality and tenant mix | Rent roll data, property address, asking rents | Multifamily Benchmarks, Underwriting Calculations |
| [OpEx Analyst](../skills/due-diligence/opex-analyst.md) | Benchmark and validate operating expenses | T-12 operating statement, property class, unit count | Multifamily Benchmarks |
| [Market Study](../skills/due-diligence/market-study.md) | Understand submarket fundamentals and comps | Property address, unit mix, asking rents | Multifamily Benchmarks |
| [Physical Inspection](../skills/due-diligence/physical-inspection.md) | Assess property condition and CapEx needs | Inspection report or property age/condition details | Multifamily Benchmarks |
| [Environmental Review](../skills/due-diligence/environmental-review.md) | Evaluate environmental risk | Phase I ESA report or property history | Risk Scoring Framework |
| [Legal & Title Review](../skills/due-diligence/legal-title-review.md) | Analyze title and encumbrances | Title commitment, survey, deed restrictions | Legal Checklist |
| [Tenant Credit](../skills/due-diligence/tenant-credit.md) | Assess tenant creditworthiness and rollover risk | Rent roll with lease terms, tenant details | Risk Scoring Framework |

## Underwriting

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [Financial Model Builder](../skills/underwriting/financial-model-builder.md) | Build a pro forma and calculate returns | Rent roll analysis, OpEx data, purchase price, financing terms | Underwriting Calculations, Multifamily Benchmarks |
| [Scenario Analyst](../skills/underwriting/scenario-analyst.md) | Stress-test the deal across 27 scenarios | Base case pro forma, assumption ranges | Underwriting Calculations |
| [IC Memo Writer](../skills/underwriting/ic-memo-writer.md) | Write an investment committee memo | All DD and UW outputs, deal thesis | Underwriting Calculations, Risk Scoring |

## Financing

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [Lender Outreach](../skills/financing/lender-outreach.md) | Identify which lenders to approach | Property profile, NOI, target leverage, deal strategy | Lender Criteria |
| [Quote Comparator](../skills/financing/quote-comparator.md) | Compare lender quotes apples-to-apples | 2+ lender quotes, NOI, purchase price, hold period | Lender Criteria, Underwriting Calculations |
| [Term Sheet Builder](../skills/financing/term-sheet-builder.md) | Assemble or review a term sheet | Selected lender quote, deal terms, negotiation priorities | Lender Criteria |

## Legal

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [PSA Reviewer](../skills/legal/psa-reviewer.md) | Review a Purchase & Sale Agreement | PSA document, key deal terms | Legal Checklist |
| [Title & Survey Reviewer](../skills/legal/title-survey-reviewer.md) | Review title commitment and ALTA survey | Title commitment, survey document | Legal Checklist |
| [Estoppel Tracker](../skills/legal/estoppel-tracker.md) | Track and validate estoppel certificates | Tenant list, rent roll, estoppel certificates | Legal Checklist |
| [Loan Doc Reviewer](../skills/legal/loan-doc-reviewer.md) | Review loan documents against term sheet | Loan documents, approved term sheet | Legal Checklist, Lender Criteria |
| [Insurance Coordinator](../skills/legal/insurance-coordinator.md) | Verify insurance compliance | Lender requirements, PSA insurance provisions, current policies | Legal Checklist |
| [Transfer Doc Preparer](../skills/legal/transfer-doc-preparer.md) | Prepare closing transfer documents | Entity details, deal terms, title info | Legal Checklist |

## Closing

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [Closing Coordinator](../skills/closing/closing-coordinator.md) | Manage the closing checklist | Status of all workstreams (DD, UW, financing, legal) | Legal Checklist |
| [Funds Flow Manager](../skills/closing/funds-flow-manager.md) | Prepare funds flow and settlement statement | Purchase price, loan terms, prorations, closing costs | Underwriting Calculations |

## Document Ingestion

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [Document Classifier](../skills/document-ingestion/document-classifier.md) | Classify deal documents by type | Any deal document (PDF, spreadsheet, memo) | — |
| [Rent Roll Parser](../skills/document-ingestion/rent-roll-parser.md) | Extract structured data from a rent roll | Rent roll file (CSV, Excel, PDF) | — |
| [Financials Parser](../skills/document-ingestion/financials-parser.md) | Extract T-12 operating statement data | Financial statement file | — |
| [Offering Memo Parser](../skills/document-ingestion/offering-memo-parser.md) | Extract data from an offering memorandum | Offering memo document | — |

## Industrial v1

| Skill | Use When You Need To... | Key Inputs | Pair With |
|-------|------------------------|------------|-----------|
| [Industrial Market Study](../skills/industrial/industrial-market-study.md) | Evaluate the submarket, competing stock, logistics position, and release depth | Property address, subtype, building specs | Industrial Benchmarks |
| [Industrial Lease Roster Analyst](../skills/industrial/industrial-lease-roster-analyst.md) | Measure WALT, concentration, rollover, and release risk | Lease roster, rent roll, tenant schedule | Industrial Lease Structures, Industrial Benchmarks |
| [Industrial Lease Abstract Reviewer](../skills/industrial/industrial-lease-abstract-reviewer.md) | Abstract reimbursements, repairs, options, transfer rights, estoppel, and SNDA items | Lease documents and amendments | Industrial Lease Structures |
| [Industrial Tenant Credit Analyst](../skills/industrial/industrial-tenant-credit-analyst.md) | Assess tenant durability, facility dependence, and downside release risk | Major tenant information, lease terms, building context | Industrial Benchmarks, Industrial Lease Structures |
| [Industrial Physical Inspection](../skills/industrial/industrial-physical-inspection.md) | Evaluate condition, functional competitiveness, and CapEx | Inspection or engineering findings, building specs | Industrial Benchmarks |
| [Industrial Underwriting Model Builder](../skills/industrial/industrial-underwriting-model-builder.md) | Build a lease-driven industrial acquisition model | Lease roster, market data, CapEx view, deal terms | Industrial Benchmarks, Industrial Lease Structures, Industrial Lender Criteria |
| [Industrial Financing Fit](../skills/industrial/industrial-financing-fit.md) | Identify likely lender categories and financing structures | WALT, tenant quality, property profile, leverage target | Industrial Lender Criteria |
| [Industrial IC Memo Writer](../skills/industrial/industrial-ic-memo-writer.md) | Synthesize industrial diligence into a decision memo | Market, lease, physical, underwriting, and financing outputs | Industrial Benchmarks, Industrial Lease Structures, Industrial Lender Criteria |

---

## Common Workflows

### "I just got a new deal package"
1. **Document Classifier** → identify what's in the package
2. **Rent Roll Parser** + **Financials Parser** + **Offering Memo Parser** → extract structured data
3. **Rent Roll Analyst** + **OpEx Analyst** → validate the numbers
4. **Financial Model Builder** → build the pro forma

### "I need to underwrite this deal fast"
1. **Rent Roll Analyst** → revenue quality
2. **OpEx Analyst** → expense validation
3. **Financial Model Builder** → pro forma and returns
4. **Scenario Analyst** → stress test

### "We're ready to present to the investment committee"
1. **IC Memo Writer** → synthesize everything into a structured memo
2. Load all prior analysis outputs as context

### "We need to source debt"
1. **Lender Outreach** → identify lenders
2. **Quote Comparator** → compare received quotes
3. **Term Sheet Builder** → finalize terms

### "We're heading into closing"
1. **PSA Reviewer** → review the purchase agreement
2. **Title & Survey Reviewer** → clear title issues
3. **Estoppel Tracker** → manage tenant estoppels
4. **Loan Doc Reviewer** → review loan docs
5. **Insurance Coordinator** → verify coverage
6. **Transfer Doc Preparer** → prepare transfer docs
7. **Closing Coordinator** → manage the checklist
8. **Funds Flow Manager** → prepare settlement statement

### "I need a U.S. industrial acquisition workflow"
1. **Document Classifier** → inventory the deal package
2. **Industrial Market Study** → evaluate demand, supply, and subtype fit
3. **Industrial Lease Roster Analyst** → measure WALT, concentration, and rollover
4. **Industrial Lease Abstract Reviewer** → abstract lease economics and transaction-critical clauses
5. **Industrial Tenant Credit Analyst** → assess tenant durability and release risk
6. **Industrial Physical Inspection** → identify condition and functional competitiveness issues
7. **Industrial Underwriting Model Builder** → build the lease-driven base case
8. **Industrial Financing Fit** → identify likely lender lanes
9. **Industrial IC Memo Writer** → summarize the investment case
