# Team Work Allocation

| Member | Research stream | Main question | Output used by the team |
|---|---|---|---|
| Mod | Healthcare context, vulnerable population, and safe operational scope | What health problem should the Heat Risk Dashboard support, and what should it avoid claiming? | Health problem framing, vulnerable-group logic, mock data-field boundaries, and clinical/public-health non-goals |
| My | Heat-risk indicators, data sources, and backend ingestion feasibility | What heat-risk data can the dashboard use, and how can it be fetched or refreshed? | Indicator inventory, source comparison, API/file feasibility, update cadence, and raw-to-dashboard data notes |
| Belle | IT use case, product requirements, and frontend dashboard behavior | What is the smallest credible dashboard product that users can operate? | User stories, must-have features, acceptance criteria, screen-level requirements, and prototype success definition |
| Chris | Stakeholders, communication logistics, adoption, and CSAT-style evaluation | Who needs to receive or act on heat-risk information, and how do we know the service is useful? | Stakeholder journey, contact-point map, channel/fallback matrix, adoption risks, and satisfaction measures |
| Com | IT architecture, data model, integration, and governance controls | What technical structure makes the initiative coherent, secure, and feasible as a Phase 0 prototype? | Conceptual architecture, data model, integration boundary, access/audit controls, and governance checklist |
| June | Evidence synthesis, policy references, and Phase 0 evaluation | What does the literature say, where are the gaps, and how should the roadmap be evaluated? | Literature review, evidence matrix, source-quality notes, feasibility assumptions, and evaluation framework |

## Shared boundaries

- Everyone researches the Heat Risk Dashboard, but each person answers a different main question.
- Everyone may identify implications for the five supporting components, but only at contact-point and handoff level.
- No one is expected to design clinical treatment, predict weather, or build a complete health information system.
- Sources must be traceable and original files must remain unchanged in `00_raw_materials/`.
- Mod owns the health framing because the role needs nursing judgment; My, Belle, and Com own the heavier IT streams because their backgrounds are computer science, development, and backend work.
- Chris owns service communication, logistics, adoption, and satisfaction because that stream benefits from CSAT SaaS and logistics experience.
- June owns evidence synthesis and evaluation because the role benefits from research-assistant strengths and does not require deep health or production-IT assumptions.

## Handoff order

1. Member submits raw source files and source register.
2. Member submits one Markdown summary per source.
3. Member submits one literature review that compares those summaries.
4. Codex checks consistency, traceability, duplicates, and gaps.
5. Team confirms matrix decisions before the information becomes a production input.
