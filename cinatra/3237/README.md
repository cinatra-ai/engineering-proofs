# Pull request 3237 — second proof round (2026-09-06 re-grade on the second round's frames)

Every picture: the real surface on a dev boot, both palettes, at proof head ef251768; graded against design main 033a697c. Each line states what the drawing requires and what the picture shows.

- `v2-agent-card-three-line-clamp-{light,dark}` — requires: the All Agents card caps its description at three lines. Shows: `line-clamp-3`, the fourth line clipped with an ellipsis on every card (#3227).
- `v2-agents-all-agents-tab-rule-and-toolbar-{light,dark}` — requires: a toolbar under the page header replaces the etched paired rule, never stacked. Shows: the toolbar directly under the strip, no rule (#3228).
- `v2-agents-executions-tab-rule-and-toolbar-{light,dark}` — requires: the same on the Executions tab. Shows: rule 0, toolbar 1 ("Run agent · Create agent · Edit dashboard") — the state the first round measured as a miss, now correct (#3228).
- `v2-agents-reviews-tab-rule-and-toolbar-{light,dark}` — requires: a view without a toolbar keeps its rule. Shows: rule 1, toolbar 0 on Reviews (#3228).
- `v2-artifacts-scope-control-workspace-{light,dark}` — requires: `Search artifacts · Type: All · Scope: Workspace` in that order. Shows: the trigger reads `Scope: Workspace`, controls in the drawing's order (#3229).
- `v2-artifacts-scope-control-picked-{light,dark}` — requires: the picked reading names the scope. Shows: `Scope: Only me` (#3229).
- `v2-chat-markdown-table-{light,dark}` — requires: nothing between the frame and the table; never centre body cells; right-align numerics and timestamps. Shows: a real assistant turn, no strip above the table, no copy or download control in the frame, `12` and `Sep 3, 2026` right-aligned (#3230).
- `v2-connector-record-list-empty-state-{light,dark}` — requires: the Empty primitive with one primary action. Shows: `Add entry` alone, dashed rounded media, 14 px headline (#3231).
- `v2-connector-record-list-delete-alertdialog-{light,dark}` — requires: a destructive AlertDialog, Cancel beside a red Delete, connector-neutral copy, never a browser prompt. Shows: `Delete this entry? … This cannot be undone.`, no browser prompt fired (#3231).

Recorded, not counted (pre-existing on the main line): the artifacts page's header rule over the toolbar (#3283).
