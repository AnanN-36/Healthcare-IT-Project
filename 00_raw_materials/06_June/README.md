# June: Vulnerable Population, Data Fields, and Evidence Synthesis

## Research mission

Build a traceable evidence base for the population context and data fields that a Heat Risk Dashboard may need. Keep the work descriptive and evidence-led, without requiring deep clinical or technical expertise.

## What to collect

- Heat-vulnerable groups, with emphasis on older adults and people with chronic conditions.
- Non-clinical or minimally clinical factors relevant to operational prioritization: age band, condition category, living alone, cooling access, mobility, or support needs.
- Evidence about barriers to receiving heat warnings or support.
- User needs for residents, caregivers, community health workers, public health officers, and facilities.
- Data minimization, consent, privacy, equity, and bias considerations for mock data.
- Gaps, contradictions, and source-quality issues across the collected evidence.

## Out of scope

- Diagnosing a person or recommending treatment.
- Building a complete patient registry.
- Assigning real-world risk scores without a qualified local authority.

## Expected research output

- A vulnerable-population profile and evidence table.
- A minimum data-field list for mock cases.
- A persona and user-need summary.
- A cross-source evidence-gap and assumption summary.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on populations vulnerable to heat and the information needed for operational outreach prioritization. Extract population definitions, relevant vulnerability factors, barriers, equity implications, and data-minimization considerations. Distinguish evidence from assumptions and note source quality or disagreement. Do not produce diagnosis or treatment advice.
```

Then combine all per-source summaries into `June_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`June_source_01_vulnerable_groups.pdf`, `June_source_02_equity_notes.md`, or `June_evidence_review_notes.md`.
