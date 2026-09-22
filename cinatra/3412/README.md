# Proof round 2 for pull request 3412: the per-scope Artifacts and Skills tabs

Head commit: `af9449ab3b99f4bbc54faee422766c1f98d097da`. Every frame in this folder is bound to this head.

## Result

- Round 1 counted three defects on the workspace Artifacts tab. Defect 1 (the type label) and defect 2 (the glyph) are cleared: each workspace row now draws the same title line and the same glyph as the same row on the organization tab.
- Defect 3 is still open, by design. Every agent-produced row carries a mono `text/plain` label. The drawing gives that label to file-form rows (uploads) only. The label comes from the shared library row, so it also shows on the organization tab. The change belongs to that shared row, and it is routed to the owner of that row.
- The personal Artifacts tab and the workspace Skills tab pass in both palettes.

## How the pages were reached

- A development installation of this head, on a fresh database, signed in as a throwaway admin account ("Proof Admin", an address at example.invalid).
- The rows come from one real agent run: the Blog Idea Generator agent, started from its own run form (brief "Blog ideas for small bakeries that want more regular customers through a newsletter", "Run right after setup"). The run completed and stored five Blog Idea artifacts, owned by the organization "Default". The viewer is the owner of that organization.
- The file-form contrast row is one real PDF, uploaded with the Upload control of the organization Artifacts tab. The product filed it as the uploader's own artifact (owner level "user", private), so it lists on the personal and workspace tabs and not on the organization tab.
- To let the run start and store its artifacts, this boot also ran the agent runtime service and a local package registry that held the agent's pinned package (0.2.0). A development boot has neither by default.
- Clicks only, from the sidebar: Organizations, the "Default" row, the Artifacts tab; Workspace, the Artifacts tab, the Skills tab; Personal, the Artifacts tab. The light control frame is a reload of the organization Artifacts tab after that walk.
- The palette comes from the product's own stored theme setting. The page root carried the class `cinatra` (light) or `dark` (dark) on every frame.
- A solid grey block covers the signed-in account (initials, name and address) in the sidebar before every capture. No other name or address shows in the frames.
- The framework's development indicator was switched off through its own route before the first capture. The wrench in the top bar exists only on a development installation.
- The installation is not attached to the live marketplace. No frame shows a marketplace surface, and the pages shot show no effect of that setting.

## Files

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `workspace-artifacts-rows-light-r2.png` | Counted (CELL1). The five-entry tablist with no Settings entry. The union the viewer owns across scopes. Each row: the type's glyph, the name, the type's defining extension label, a muted meta line, Open at the right edge. The same title line and glyph as the organization control. A mono MIME label on the upload only. | Five entries, Artifacts selected. Six rows, newest first: the personal PDF and the five organization Blog Idea rows. Each Blog Idea row reads "Blog Idea" with the same glyph and tint as the control. The PDF row carries `application/pdf`. Every Blog Idea row also carries `text/plain`. | Fail (defect 3 only) |
| `workspace-artifacts-rows-dark-r2.png` | Counted (CELL1). The same, dark palette. | The same reading holds. | Fail (defect 3 only) |
| `personal-artifacts-light-r2.png` | Counted (CELL2). The five-entry tablist. Only the rows the viewer owns personally; none of the organization's rows. | Five entries, Artifacts selected. One row: the uploaded PDF with `application/pdf`. None of the five organization rows. | Pass |
| `personal-artifacts-dark-r2.png` | Counted (CELL2). The same, dark palette. | The same reading holds. | Pass |
| `workspace-skills-light-r2.png` | Counted (CELL3). The five-entry tablist. At least one installed skill that the viewer's scopes own. | Five entries, Skills selected. Five skill rows, each marked with the workspace owner badge: blog-idea-authoring, blog-idea-matcher, blog-image-matcher, blog-post-matcher, blog-content. | Pass |
| `workspace-skills-dark-r2.png` | Counted (CELL3). The same, dark palette. | The same reading holds. | Pass |
| `organization-artifacts-control-light-r2.png` | Recorded (CELL5, the control). The organization tab lists what the organization owns; Settings is the last tab. | Six entries with Settings last. The five Blog Idea rows with "Blog Idea", the same glyph, and the same `text/plain` label. The personal PDF is not listed. | Recorded, matches CELL1 |
| `organization-artifacts-control-dark-r2.png` | Recorded (CELL5). The same, dark palette. | The same reading holds. | Recorded, matches CELL1 |

## Not reached in this round

- CELL1 with two organizations, one agent row in each: not shot. Memory on the machine was below the round's starting floor after the counted frames, so no more pages were loaded.
- The personal Artifacts empty pattern: not shot. The uploaded PDF is personally owned, so the tab is populated. Round 1 passed the empty pattern.

## Recorded, not counted

- The type's own list-row mark did not draw on any surface in this round, the control included. At this head the committed renderer build map has no list-row entry, and this boot had no runtime renderer entry. Every row draws the generic mark in the tint of a typed row. So defect 2 is cleared by parity with the control; this round cannot show the type's own mark.
- The meta line names the owner level and the visibility ("Organization · organization", "User · private"). The drawing's examples name the owner ("Organization: Acme Corp", "Private"). This is the shared row, and it is the same on the control.
- The upload row also names its defining extension ("PDF") and uses the generic mark in the tint of a typed row. The drawing's upload example shows only the mono MIME label and a file mark in a rust tint. The upload row reads "updated", the example reads "uploaded".
- An upload started from the organization tab is filed as the uploader's own artifact, so that tab does not list it after a reload.
- The shared list toolbar (search, Type, Scope, drop hint, Upload) rides into every scope tab, as round 1 recorded. Its Scope picker reads "Scope: Workspace" on the organization and personal tabs.
- The Open control was not pressed in this round.
