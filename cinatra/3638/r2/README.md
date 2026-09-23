# Sharing tab: the recommendation line, its pre-selected picker and its lock

Frames of the real page, taken on a production build of commit
`c781add0005de9766fb248c415b7fccd33d4307c`. That commit is the head of the
lock-glyph change; it contains the head of the recommendation-line change
(`d957bdc74bade16dbc1bd6383c46ca2277b56d43`), and it sits on the fixed Sharing
tab base, where the package draws the permissions card itself. Every frame on
this page belongs to that one commit.

This round repeats an earlier round that ran before the base landed. The
reading is the same, and nothing a person sees differs from that round.

## How the page was reached

1. A throwaway account registered on a fresh installation and became the
   platform administrator and the owner of the organization "Default".
2. A Personal MCP server was added through the connector's own Setup form:
   a label, a server address that points at a throwaway server on this
   machine, a made-up token in the API key field, and the scope
   "Personal (only me)". The made-up token is not a credential and appears in
   no frame.
3. That gave one stored connection with an untouched sharing seed.
4. From the connector page the Sharing tab was opened through the tab strip.
5. The palette was switched by the stored theme setting and read back on the
   `<html>` element before each frame: `cinatra` for light, `dark` for dark.

Solid blocks cover the account name and the e-mail address in every frame.
Nothing else is painted over.

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `sharing-tab-untouched-seed-recommendation-line-light.png` | A connection just added, before any save: the picker pre-selected to the recommended scope, and under it the recommendation line word for word as the drawing gives it | Trigger "Workspace: All"; the line reads "This connector recommends sharing with your organization", the drawing's dash, "nothing is shared until you save. Currently: only you."; the helper line under it; one right-aligned "Save changes" | pass |
| `sharing-tab-untouched-seed-recommendation-line-dark.png` | The same, dark | The same, on the dark ground | pass |
| `sharing-tab-untouched-seed-line-no-lock-enlarged-cut-light.png` | The line carries no lock in front of it | An enlarged cut of the light frame above: the line starts at the same left edge as the helper line under it, with nothing in front of it | pass |
| `sharing-tab-untouched-seed-line-no-lock-enlarged-cut-dark.png` | The same, dark | The same, on the dark ground | pass |
| `sharing-tab-untouched-seed-picker-open-light.png` | The picker is pre-selected, not merely labelled | The open list: "Workspace: All" checked; "Organization: Default" and "Workspace: Admins only" held as "Included via Workspace: All"; "Personal: Only me" unchecked | pass |
| `sharing-tab-after-save-no-line-dark.png` | After "Save changes" with nothing changed: the saved scope and no line | Trigger "Workspace: All"; the recommendation line is gone; the helper line, Ownership and the owner row stay | pass |
| `sharing-tab-after-save-no-line-light.png` | The same, light | The same, on the light ground | pass |
| `sharing-tab-two-connections-rollup-recorded-light.png` | Recorded, not graded: the page with two connections | The roll-up card "Connections status, 2 Connected" above two panels, while the tab strip reads Setup, Sharing, Help | recorded |
| `sharing-tab-decline-unchecked-before-save-light.png` | Recorded, not graded: the decline road before the save | On a second new connection the trigger reads "Personal: Only me" after the recommended row is unchecked, and the recommendation line still stands, because nothing is saved yet | recorded |
| `sharing-tab-decline-after-save-personal-no-line-light.png` | Recorded, not graded: the decline road after the save | "Personal: Only me" and no line; the first connection keeps "Workspace: All" | recorded |

The two enlarged cuts are cuts of the two frames above them, drawn at twice the
size. They are not separate shots.

## What is not here

The ceiling line with its one lock is not in these frames. No shipped connector
that declares a ceiling can hold a real connection on a local installation, so
the product cannot reach that state here. It draws on the design conformance
test page only, which is not proof of the real page.

## Reading the frames

The two enlarged cuts carry the grading for the lock: the recommendation line
begins at the same left edge as the helper line beneath it. A lock and its gap
would push the first word to the right. The lock on the row of the person who
connected the connection is a different lock and stays; it sits at the right
edge of that row in every frame.
