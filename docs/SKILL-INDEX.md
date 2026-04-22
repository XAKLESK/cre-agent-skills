# Skill Index - Quick Reference

This index groups the repo by practical use:

- **Multifamily Core** for the original acquisitions pack
- **Shared CRE** for broadly reusable legal, closing, and intake tools
- **Industrial v1** for the new U.S. industrial acquisitions workflow

---

## Multifamily Core

### Due Diligence

| Skill | Use When You Need To... | Pair With |
|-------|--------------------------|-----------|
| Rent Roll Analyst | Validate revenue quality, occupancy, and loss to lease | Multifamily Benchmarks, Underwriting Calculations |
| OpEx Analyst | Benchmark and normalize operating expenses | Multifamily Benchmarks |
| Market Study | Evaluate multifamily submarket fundamentals | Multifamily Benchmarks |
| Physical Inspection | Estimate CapEx and deferred maintenance | Multifamily Benchmarks |
| Environmental Review | Assess environmental liabilities | Risk Scoring |
| Legal & Title Review | Identify title, zoning, and encumbrance issues | Legal Checklist |
| Tenant Credit | Review tenant quality and concentration in a multifamily context | Risk Scoring |

### Underwriting and Financing

| Skill | Use When You Need To... | Pair With |
|-------|--------------------------|-----------|
| Financial Model Builder | Build a multifamily base-case model | Underwriting Calculations, Multifamily Benchmarks |
| Scenario Analyst | Stress-test a multifamily model | Underwriting Calculations |
| IC Memo Writer | Summarize the multifamily investment case | Underwriting Calculations, Risk Scoring |
| Lender Outreach | Identify multifamily lender categories | Lender Criteria |
| Quote Comparator | Compare multifamily loan quotes | Lender Criteria, Underwriting Calculations |
| Term Sheet Builder | Assemble or review multifamily debt terms | Lender Criteria |

---

## Shared CRE

### Legal

| Skill | Use When You Need To... |
|-------|--------------------------|
| PSA Reviewer | Review a purchase and sale agreement |
| Title & Survey Reviewer | Review title and survey issues |
| Estoppel Tracker | Track estoppels and compare them to leases |
| Loan Doc Reviewer | Review lender documents against business terms |
| Insurance Coordinator | Coordinate insurance requirements |
| Transfer Doc Preparer | Prepare transfer and closing documents |

### Closing

| Skill | Use When You Need To... |
|-------|--------------------------|
| Closing Coordinator | Track closing readiness across workstreams |
| Funds Flow Manager | Produce a settlement statement and funds flow |

### Document Ingestion

| Skill | Use When You Need To... | Notes |
|-------|--------------------------|-------|
| Document Classifier | Inventory and classify incoming deal files | Broad CRE intake utility |
| Rent Roll Parser | Extract structured rent-roll data | Best fit for multifamily-style unit data |
| Financials Parser | Extract revenue and expense data from operating statements | Broad CRE intake utility |
| Offering Memo Parser | Pull key facts from an OM or marketing package | Broad CRE intake utility |

---

## Industrial v1

### Industrial Acquisitions Core

| Skill | Use When You Need To... | Pair With |
|-------|--------------------------|-----------|
| Industrial Market Study | Evaluate local supply, demand, and subtype fit | Industrial Benchmarks |
| Industrial Lease Roster Analyst | Measure WALT, concentration, and rollover risk | Industrial Lease Structures, Industrial Benchmarks |
| Industrial Lease Abstract Reviewer | Abstract lease economics, repairs, options, and transfer rights | Industrial Lease Structures |
| Industrial Tenant Credit Analyst | Assess tenant durability and release risk | Industrial Benchmarks, Industrial Lease Structures |
| Industrial Physical Inspection | Assess condition and functional competitiveness | Industrial Benchmarks |
| Industrial Underwriting Model Builder | Build a lease-driven industrial model | Industrial Benchmarks, Industrial Lease Structures, Industrial Lender Criteria |
| Industrial Financing Fit | Match the deal to likely lender categories | Industrial Lender Criteria |
| Industrial IC Memo Writer | Summarize the industrial investment case | All three industrial knowledge bases |

---

## Common Workflows

### New Multifamily Deal Package

1. `document-classifier`
2. `rent-roll-parser`
3. `financials-parser`
4. `offering-memo-parser`
5. `rent-roll-analyst`
6. `opex-analyst`
7. `financial-model-builder`

### New Industrial Acquisition

1. `document-classifier`
2. `financials-parser`
3. `offering-memo-parser`
4. `industrial-market-study`
5. `industrial-lease-roster-analyst`
6. `industrial-lease-abstract-reviewer`
7. `industrial-tenant-credit-analyst`
8. `industrial-physical-inspection`
9. `industrial-underwriting-model-builder`
10. `industrial-financing-fit`
11. `industrial-ic-memo-writer`

### Closing and Execution

1. `psa-reviewer`
2. `title-survey-reviewer`
3. `loan-doc-reviewer`
4. `insurance-coordinator`
5. `closing-coordinator`
6. `funds-flow-manager`
