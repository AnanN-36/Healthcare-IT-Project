# Chris: Stakeholders, Communication Logistics, Adoption, and CSAT-Style Evaluation

## Research mission

Study how heat-risk information moves through people, service touchpoints, communication channels, and feedback loops so that the roadmap can explain adoption, logistics, and usefulness beyond the screen itself.

## What to collect

- Stakeholders involved in heat-risk communication and response.
- Contact points between dashboard users, public health teams, community workers, facilities, residents, caregivers, and local organizations.
- Communication channels: dashboard notification, phone, SMS, LINE, email, public announcement, or other locally relevant channels.
- Service logistics: acknowledgement, escalation, fallback channel, response delay, handoff ownership, and coordination friction.
- Adoption and satisfaction signals: comprehension, trust, message usefulness, task completion, user feedback, and reasons users may ignore or abandon the service.
- Plain-language and accessibility considerations for messages, not only visual screens.

## Out of scope

- Designing detailed clinical, hospital, emergency, or community-health workflows.
- Selecting a final communications vendor.
- Assuming a digital channel reaches every vulnerable person.

## Expected research output

- A stakeholder journey and contact-point map.
- A contact-point / handoff / channel matrix.
- Primary and fallback channels for key interactions.
- A short list of service-logistics risks and adoption barriers.
- CSAT-style prototype evaluation measures for usefulness, trust, and clarity.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on stakeholders, communication logistics, contact points, channels, handoffs, ownership, acknowledgement, fallback mechanisms, adoption, satisfaction, and service usefulness. Extract who contacts whom, what information is transferred, through which channel, what can fail, and how users might evaluate the service. Keep this at contact-point level; do not design detailed operational or clinical workflows.
```

Then combine all per-source summaries into `Chris_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Chris_source_01_stakeholder_journey.pdf`, `Chris_source_02_communication_channels.md`, or `Chris_csat_adoption_notes.md`.
