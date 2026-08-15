# Com: Stakeholders, Contact Points, and Handoff Channels

## Research mission

Map who needs to communicate with whom around a heat-risk alert and what information or handoff should cross each contact point. Use a health and public-health coordination lens, but keep the stream at contact-point level; it does not design detailed workflows for the five supporting components.

## What to collect

- Stakeholders involved in heat-risk communication and response.
- Existing contact channels: dashboard notification, phone, SMS, LINE, email, radio, public announcement, or other locally relevant channels.
- Information that must be handed off at each contact point.
- Ownership and acknowledgement expectations at a high level.
- Communication barriers, language needs, digital access, and failure fallback channels.

## Out of scope

- Detailed clinical, hospital, emergency, or community-health workflows.
- Selecting a final communications vendor.
- Assuming that a digital channel reaches every vulnerable person.

## Expected research output

- A stakeholder and contact-point map.
- A contact-point / handoff matrix.
- A primary channel plus fallback channel for each interaction.
- A short list of coordination risks and unresolved questions.

## NotebookLM prompt

For each source, use the shared source-summary prompt and add:

```text
Focus on stakeholders, communication channels, handoffs, ownership, acknowledgement, and fallback mechanisms relevant to heat-risk response. Extract who contacts whom, what information is transferred, through which channel, and what can fail. Keep this at contact-point level; do not design detailed operational or clinical workflows.
```

Then combine all per-source summaries into `Com_literature_review.md` using the shared literature-review prompt.

## File rule

Keep original files unchanged in this folder. Name files clearly, for example:
`Com_source_01_stakeholder_map.pdf`, `Com_source_02_communication_channels.md`, or `Com_interview_notes_YYYY-MM-DD.md`.
