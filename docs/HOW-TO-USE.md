# How to Use CRE Agent Skills

This guide covers how to load these skill files into different AI platforms.

---

## Claude (Anthropic)

### Claude Projects (Recommended)

1. Open [claude.ai](https://claude.ai) and create a new Project
2. Click "Add knowledge" in the Project settings
3. Upload the `.md` skill file(s) you want to use
4. Optionally upload the recommended knowledge base files listed in the skill's "Related Knowledge Bases" section
5. Start a conversation in the project — Claude will automatically reference the loaded skills

**Tip:** Name your project by deal or task (e.g., "Parkview Apartments DD") and load the relevant subset of skills for that workflow.

### Claude Code (CLI)

If you're using Claude Code, you can reference skill files directly:

```bash
# Load a skill as context
claude "Using the skill in skills/due-diligence/rent-roll-analyst.md, analyze this rent roll: [data]"
```

Or add frequently-used skills to your CLAUDE.md file for automatic loading.

---

## ChatGPT (OpenAI)

### Custom GPT

1. Go to [chat.openai.com](https://chat.openai.com) → Explore GPTs → Create
2. In the "Instructions" field, paste the full content of the skill file
3. For knowledge bases, upload them as files in the GPT's "Knowledge" section
4. Save and use the GPT for that specific analysis task

### Conversation-Level

1. Start a new conversation
2. Paste the skill content as your first message: "Use the following skill instructions for our conversation: [paste skill content]"
3. Follow up with your analysis request and data

---

## Cursor / Windsurf / AI Code Editors

### As Rules Files

1. Copy the `.md` skill file into your project's rules directory (e.g., `.cursor/rules/` or `.windsurfrules/`)
2. The AI assistant will automatically reference the skill when relevant

### As Context Files

1. Open the skill file in your editor
2. Reference it in your prompt: "Following the instructions in rent-roll-analyst.md, analyze this data..."

---

## Any LLM (API Usage)

Include the skill content in your system prompt:

```python
system_prompt = open("skills/due-diligence/rent-roll-analyst.md").read()

response = client.messages.create(
    model="claude-sonnet-4-20250514",
    system=system_prompt,
    messages=[
        {"role": "user", "content": "Analyze this rent roll: [data]"}
    ]
)
```

For richer analysis, concatenate the skill with its recommended knowledge bases:

```python
skill = open("skills/due-diligence/rent-roll-analyst.md").read()
knowledge = open("knowledge/multifamily-benchmarks.md").read()

system_prompt = f"{skill}\n\n---\n\nReference Knowledge:\n{knowledge}"
```

---

## Recommended Skill Combinations

Different tasks benefit from loading multiple skills together. Here are common combinations:

### Full Due Diligence Review
Load all 7 due diligence skills + Risk Scoring Framework + Multifamily Benchmarks

### Underwriting Package
- Financial Model Builder + Scenario Analyst + IC Memo Writer
- Knowledge: Underwriting Calculations + Multifamily Benchmarks

### Debt Sourcing
- Lender Outreach + Quote Comparator + Term Sheet Builder
- Knowledge: Lender Criteria + Underwriting Calculations

### Legal Review
- PSA Reviewer + Title & Survey Reviewer + Estoppel Tracker
- Knowledge: Legal Checklist

### Document Processing
- Document Classifier + Rent Roll Parser + Financials Parser + Offering Memo Parser
- These work well as a pipeline: classify first, then parse each document type

### Quick Deal Screening
- Rent Roll Analyst + OpEx Analyst + Financial Model Builder
- Knowledge: Underwriting Calculations + Multifamily Benchmarks
- Gets you to a preliminary NOI and cap rate assessment fast

---

## Tips for Best Results

1. **Provide structured data when possible.** CSV or tabular data produces better analysis than unstructured text.

2. **Include the property address.** Many skills use web research to pull market comps, submarket data, and benchmarks. The more specific the location, the better.

3. **Load knowledge bases for deeper analysis.** Skills work on their own, but pairing them with the recommended knowledge files gives the AI access to formulas, benchmarks, and criteria it can reference during analysis.

4. **Trust the output format.** Each skill defines a structured output (JSON or Markdown). Let the AI follow that format — it makes results consistent and comparable across deals.

5. **Review the confidence scoring.** Every skill rates its own confidence (HIGH/MEDIUM/LOW) and flags data gaps. Pay attention to these — they tell you where the analysis is weakest.

6. **Iterate on data gaps.** If the skill flags missing data, provide additional information and re-run that section. The skills are designed to handle partial data gracefully.
