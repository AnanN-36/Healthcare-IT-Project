# NotebookLM Prompt Playbook

Use this playbook after sources have been placed in the six member folders under `00_raw_materials/`.

## Rules for every source

- Process one source at a time.
- Keep the original source unchanged.
- Do not ask the AI agent to fill missing facts from memory.
- Require page, section, table, figure, or URL location for important claims.
- Mark unsupported conclusions as `Assumption`, `Interpretation`, or `Open question`.
- Do not include personal or confidential data.

## Shared prompt: one-source summary

```text
You are supporting a student team designing a Heat Risk Dashboard as an IT and operational-support Roadmap Initiative applied to healthcare and public health.

Analyze only the supplied source. Do not use outside facts and do not invent missing information. Produce a structured Markdown summary with:

1. Source metadata: title, author or organization, date, URL or identifier, and source type.
2. The research question this source helps answer.
3. Five to ten key findings, each with a precise source location.
4. Evidence, recommendations, assumptions, and interpretations separated clearly.
5. Implications for the Heat Risk Dashboard.
6. Data fields, user needs, workflow needs, governance requirements, or evaluation measures suggested by the source.
7. Limitations, uncertainty, contradictions, and missing information.
8. Three to five follow-up questions for the team.

Do not provide diagnosis, treatment advice, a clinical decision rule, a weather prediction, or a claim of legal compliance. Keep the project boundary visible: one main component is the Heat Risk Dashboard; five supporting components are described only as contact points and handoffs.
```

Append exactly one member-specific prompt from the relevant `00_raw_materials/<member>/README.md`.

## Shared prompt: member literature review

```text
Using only the supplied per-source Markdown summaries, write a literature review for the Heat Risk Dashboard Roadmap Initiative.

Compare the sources instead of repeating them. Organize the review as:

1. Scope and research question.
2. Search or source coverage, including what was not found.
3. Thematic findings.
4. Areas of agreement and disagreement.
5. Strongest evidence with source traceability.
6. Implications for the Heat Risk Dashboard.
7. Implications for the five supporting contact points and handoffs, without designing detailed workflows.
8. Evidence gaps, risks, and assumptions.
9. Recommended inputs to the relevant project matrices.
10. A concise conclusion.

For every important claim, cite the summary filename and its original source location. Do not add outside facts. Distinguish evidence from interpretation and recommendation. Do not turn the review into a clinical guideline or production architecture.
```

## Suggested analysis folder layout

```text
02_analyzed_data_notebooklm/
  01_Mod/
    Mod_source_01_summary.md
    Mod_source_02_summary.md
    Mod_literature_review.md
  02_My/
    My_source_01_summary.md
    My_literature_review.md
  03_Belle/
    Belle_source_01_summary.md
    Belle_literature_review.md
  04_Chris/
    Chris_source_01_summary.md
    Chris_literature_review.md
  05_Com/
    Com_source_01_summary.md
    Com_literature_review.md
  06_June/
    June_source_01_summary.md
    June_literature_review.md
```

Create the per-source summaries first. Create the literature review only after the member has finished the initial source set.
