# Belle: Vulnerable Population and Dashboard Data Fields

## Research mission

Define which population attributes are needed to support heat-risk prioritization at a high level, while keeping the concept safe, explainable, and privacy-aware.

## What to collect

- Heat-vulnerable groups, with emphasis on older adults and people with chronic conditions.
- Non-clinical or minimally clinical factors that affect outreach priority: age band, relevant condition category, living alone, cooling access, mobility or support needs.
- Evidence about barriers to receiving heat warnings or support.
- User needs for residents, caregivers, community health workers, public health officers, and facilities.
- Data minimization, consent, privacy, and equity considerations for a registry or mock dataset.

## Out of scope

- Diagnosing a person or recommending treatment.
- Building a complete patient registry.
- Assigning real-world risk scores without a qualified local authority.

## Expected research output

- A vulnerable-population profile and evidence table.
- A minimum data-field list for mock cases.
- A persona and user-need summary.
- Risks of exclusion, bias, stigmatization, or unsafe prioritization.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on populations vulnerable to heat and the information needed for operational outreach prioritization. Extract population definitions, relevant vulnerability factors, barriers, equity implications, and data-minimization considerations. Distinguish evidence from assumptions. Do not produce diagnosis or treatment advice.
```

Then combine all per-source summaries into `Belle_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Do not place real personal or patient-identifiable data in the repository. Name files clearly, for example:
`Belle_source_01_vulnerable_groups.pdf` or `Belle_source_02_equity_notes.md`.
