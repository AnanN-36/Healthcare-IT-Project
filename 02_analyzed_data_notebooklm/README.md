# Analyzed Data From NotebookLM

Store materials that have already been digested or summarized through NotebookLM here.

Examples:

- source summaries
- extracted key points
- FAQ-style notes
- claim/evidence tables
- quotes or references selected for pitch slides

Rule: every analyzed file should mention which raw source file or link it came from.

## Required sequence

1. Create one Markdown summary for each raw source.
2. Keep the same member prefix as the raw source, such as `My_source_01_summary.md`.
3. After the individual summaries are complete, combine them into one member literature review.
4. Use `notebooklm_prompt_playbook.md` for the shared prompt and the member-specific prompt.

The literature review should compare evidence and identify gaps. It should not simply concatenate the individual summaries.
