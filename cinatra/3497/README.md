# Proof round — per-scope Assistants and Agents tabs (pull request 3497, issue 2808)

Head under proof: c6e5e9b4e57591086afd1e5c5c2b9613615276d7.

The palette was switched through the application's own theme control. The
development indicator is off through the framework's own means (its box
measures zero in every reading). The account band at the foot of the sidebar is
painted over in every frame. No agent run was dispatched in this proof round.

The wrench in the top bar is the development-installation control; it exists
because this proof round ran on a development installation, and it is not part
of any criterion.

## Frames

| file | page | state | palette |
| --- | --- | --- | --- |
| cell1-workspace-agents-tab-light.png | /workspace/agents | every agent card's right panel: Run, then the text links Settings and More details side by side with Settings to the left; no version and no status indicator | light |
| cell1-workspace-agents-tab-dark.png | /workspace/agents | the same | dark |
| cell2-workspace-assistants-tab-builtin-row-light.png | /workspace/assistants | the built-in Cinatra assistant row: its description in the middle panel, Chat as the primary action, then Settings and More details side by side | light |
| cell2-workspace-assistants-tab-builtin-row-dark.png | /workspace/assistants | the same | dark |
| cell3-agent-assignment-page-workspace-after-settings-click-light.png | /workspace/agents/cinatra-ai/code-reviewer-agent/settings?tab=skills | reached by a real click on the Settings text link of the first card; the page renders its scope heading, the line "Settings for @cinatra-ai/code-reviewer-agent in this scope." and a placeholder body reading "This surface is not ready yet" with a Back to Agents control | light |

## Readings

Every shutter appended one reading to dom-readings.jsonl: the address, the
breadcrumb, the palette, each card row with its controls, their addresses and
their boxes.

Agents tab, light and dark: 30 card rows, each identical in structure — Run (a
link to that agent's new-run address), then Settings and More details. All 30
Settings addresses end in `?tab=skills`, one per card, each naming that agent's
assignment page at the workspace scope.

Assistants tab, light and dark: one row, the built-in Cinatra assistant, with
its description in the middle panel. Its controls are Chat, Settings
(`/workspace/assistants/cinatra-ai/cinatra-assistant/settings?tab=skills`) and
More details.

Directory read-back on the round's own installation: 95 installed extension
rows in total, 31 of kind agent, none of kind assistant (the assistant row on
the tab is the built-in one), and 0 agent run rows — consistent with a round
that dispatched nothing.

## What is counted

The card's right panel, the row's right panel and the Settings address. The
assignment page's composition and the earlier legs' loader are recorded here
but are not counted.
