# Sharing tab: the recommendation line, the pre-selected picker and the lock

Head commit of every frame: b9212afeb03a218c6a6bb95acf126bd55e35df0e (pull request 3638). This head contains the head of pull request 3637, 551d7b93502f826bbf05438f184f7e3124d7987a. Between the two heads, only the five files of the lock fix differ. The recommendation model is the same file at both heads.

All frames come from a development boot of this head, taken on 2026-09-22 between 17:38 and 17:45 UTC. The boot had its own database and its own connection service. The frames are 1440 by 1000 pixels at scale 1.

## How each page was reached

1. The first account registered through the product's sign-up page. It is a fake account, and it owns the organization "Default".
2. The MCP Servers connector page (the target of the MCP Servers card on the Connectors page) was opened by its address. On its Setup tab, the connector's own form got a label, the address of a throwaway local MCP server, an obviously fake API key and the scope "Personal (only me)". Then "Add server" was pressed. The toast read "External MCP server saved.". The key is a made-up token, not a credential, and it shows in no frame.
3. The Sharing tab was opened through the page's tab strip.
4. The palette was set in the page's stored theme, followed by a reload. The root class was read back on every frame: `cinatra` for light, `dark` for dark.
5. Solid grey blocks cover the account name and the e-mail address before each shot. They sit in the sidebar footer and in the owner row.

The drawing's dash in the recommendation line is written below as "[U+2014]".

## Frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| sharing-tab-untouched-seed-recommendation-line-light.png | CELL1 (3637): on a connection just added, before any save, the picker is pre-selected to the recommended scope and the recommendation line reads word for word as the drawing gives it. CELL3 (3638): no lock in front of that line. | One panel. The trigger reads "Workspace: All". Under it: "This connector recommends sharing with your organization [U+2014] nothing is shared until you save. Currently: only you." The line has no glyph in front. The owner row keeps its lock. The stored policy is still the untouched owner seed. | pass |
| sharing-tab-untouched-seed-recommendation-line-dark.png | The same as the row above, in the dark palette. | The same as the row above, in the dark palette. | pass |
| sharing-tab-untouched-seed-line-no-lock-enlarged-cut-light.png | CELL3 (3638): an enlarged cut of the light CELL1 frame above (two times). It is not a separate shot. | The line starts at the same left edge as the helper line "Choose who can use this connection.". No lock in front of it. | pass |
| sharing-tab-untouched-seed-line-no-lock-enlarged-cut-dark.png | CELL3 (3638): an enlarged cut of the dark CELL1 frame above. | The same as the row above, in the dark palette. | pass |
| sharing-tab-untouched-seed-picker-open-light.png | Support for CELL1: the pre-selected scope in the open list. | "Workspace: All" is checked. "Organization: Default" and "Workspace: Admins only" read "Included via Workspace: All". "Personal: Only me" is not checked. Escape closed the list, and the trigger still read "Workspace: All". | pass |
| sharing-tab-after-save-no-line-dark.png | CELL2 (3637): after "Save changes" with nothing changed, the saved scope and no recommendation line. | Toast "Access policy saved.". The trigger reads "Workspace: All". There is no recommendation line. The helper line, Ownership, the owner row lock and "Save changes" stay. The stored policy is workspace, and the seed marker is gone. | pass |
| sharing-tab-after-save-no-line-light.png | The same as the row above, in the light palette (after a reload). | The same as the row above, in the light palette. | pass |
| sharing-tab-two-connections-rollup-recorded-light.png | Recorded, not counted: the roll-up card with two connections on a page whose tab strip has no Connections tab. | "Connections status" with "2 Connected" above the two panels. The tab strip reads Setup, Sharing, Help. | recorded |
| sharing-tab-decline-unchecked-before-save-light.png | Recorded, not counted: the decline road on a second new server. After the "Workspace: All" row is unchecked, the trigger reads "Personal: Only me". | On the second panel, the trigger reads "Personal: Only me". The recommendation line still shows, because nothing is saved yet. | recorded, as expected |
| sharing-tab-decline-after-save-personal-no-line-light.png | Recorded, not counted: after "Save changes", the panel shows "Personal: Only me" and no line. | Toast "Access policy saved.". The second panel reads "Personal: Only me" with no recommendation line. The first panel still reads "Workspace: All". The stored policy of the second connection is owner only, with no seed marker. | recorded, as expected |

## Not in the frames

- The ceiling line with its lock: no shipped connector with a ceiling can hold a real connection on a development installation. The connectors that declare a ceiling need a real third-party credential to connect. The MCP Servers connector only recommends a scope. The ceiling line draws only on the design conformance test page, and that page is not proof.
- Development-only chrome shows in every frame: the framework's development indicator (bottom right) and the wrench in the top bar.
