# Pull request 3289 — live proof round four (2026-09-06)

Issue #3202: an Anthropic key held by the connection service resolves at the initial-sync seams, so the setup's skill sync commits and a skill-selecting assistant turn runs.

Frames, 1440x900 CSS at device scale 2, light and dark through the app's own theme control, the framework's development indicator off on pixels:

- `cell1-llm-committed-claude-anthropic-{light,dark}.png` — the provider screen with the Anthropic provider committed (reused unchanged from round one).
- `cell2-chat-turn-skill-selecting-{light,dark}-assistant-answered.png` — the headline: a skill-selecting chat turn through the real provider settled with a written answer (44 s light, 40 s dark, separate conversations); the skill-delivery rows read delivered; no not-synced error and no classified too-early message anywhere.

`measurements.json` and `dom-readings.jsonl` carry the readings taken at each shutter. The full record is the bot comment on the pull request.
