# Pictures for pull request 3544 and issue 3397

Head commit: `d61934919fd1ebff0a6abff30614aa57aca90d76`. Every picture was taken on a local development boot of this commit.

Drawing: the connectors drawing, section "Sharing tab" (revision 8f57daa).

## How the pages were reached

- The account is an obviously fake administrator account. It was registered through the product's own sign-up page. It owns the organization "Default".
- First boot (this commit): the sidebar Connectors page, then the MCP Servers card, then the Sharing tab. This boot gave the two "before any server" pictures. It also registered the server without a key through the Setup form.
- Second boot: the same route (Connectors page, MCP Servers card), then the Setup tab and the Sharing tab.
- Third boot: the MCP Servers setup page, opened directly, then its Setup and Sharing tabs.
- The palette is the product's own theme setting (light or dark), stored in the browser before the page loads.
- Every server was registered on the Setup tab with the product's own form and its "Add server" button. The server URLs point to a small local test server. The key of the second server is an obviously fake value. It is not in any picture.
- The share was chosen in the Access picker and saved with the panel's own "Save changes" button. The first server was deleted with its own delete button and the confirmation.
- Grey boxes cover the account name, the e-mail address and the initials of the account. They cover the sidebar footer and each owner row. They were painted just before each capture.
- No page was faked. No fixture route, no component render, no database write and no source change was used.

## Pictures for pull request 3544

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `sharing-tab-before-any-server-empty-light.png` | A person with no saved connection here sees nothing on the Sharing tab. | Sharing tab selected, empty body, 0 panels. First boot, before any server. | PASS |
| `sharing-tab-before-any-server-empty-dark.png` | Same, dark palette. | Same, dark. | PASS |
| `setup-tab-server-registered-without-key-light.png` | The server was registered with the key field blank. | The list shows "Lane demo server, no key" with no "API key configured" badge. The key field shows its own placeholder dots. | PASS |
| `setup-tab-server-registered-without-key-dark.png` | Same, dark palette. | Same, dark. | PASS |
| `sharing-tab-keyless-server-panel-light.png` | Cell 1: the server without a key has its panel on the Sharing tab. | 1 panel: a row with the connection name and the mono line `externalMcp`, then Access (picker "Personal: Only me", recommendation line, helper line), Ownership (search field, helper line, owner row with a lock) and "Save changes". No roll-up above one connection. | PASS |
| `sharing-tab-keyless-server-panel-dark.png` | Cell 1, dark palette. | Same, dark. | PASS |
| `setup-tab-second-server-registered-with-key-light.png` | Cell 2: a second server is registered with a key. | Toast "External MCP server saved." The list has two servers. Only the second one has "API key configured". The form keeps the typed label and URL after the save. The lane cleared the key field before the capture. | PASS |
| `setup-tab-second-server-registered-with-key-dark.png` | Same, dark palette (after a reload). | Same two servers, dark. The form is empty after the reload. | PASS |
| `sharing-tab-keyless-and-keyed-servers-two-panels-light.png` | Cell 2: two servers give two panels, one for each server, with the roll-up above them. | Roll-up "Connections status" with "2 Connected", no Check button, no link. Then 2 panels, each with its own Access and Ownership card. | PASS |
| `sharing-tab-keyless-and-keyed-servers-two-panels-dark.png` | Same, dark palette. | Same, dark. | PASS |
| `setup-tab-keyless-server-deleted-light.png` | Cell 2: the server without a key is deleted. | Toast "External MCP server removed." Only the server with a key is in the list. | PASS |
| `setup-tab-keyless-server-deleted-dark.png` | Same, dark palette (after a reload). | Same list, dark. | PASS |
| `sharing-tab-after-keyless-server-deleted-one-panel-light.png` | Cell 2: the deleted server leaves no panel behind. | 1 panel (the server with a key), no roll-up. | PASS |
| `sharing-tab-after-keyless-server-deleted-one-panel-dark.png` | Same, dark palette. | Same, dark. | PASS |

Panel count across the states: 0 before any server, 1 after the server without a key, 2 after the server with a key, and 1 after the delete. The page and the database agree in each state.

Not reached: a key added to, or removed from, a server that already exists. The Setup form has no edit mode. It always registers a new server, so the product offers no way to reach this state.

## Pictures for issue 3397 (second set, same third boot)

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `connection-cells-rollup-and-panel-light.png` | The roll-up and the panel. | The same capture as the two-panel picture above: roll-up "2 Connected", then one panel for each connection. | PASS |
| `connection-cells-rollup-and-panel-dark.png` | Same, dark palette. | Same, dark. | PASS |
| `connection-cells-access-picker-open-light.png` | The share is chosen in the panel's own picker. | The open picker of the server with a key. Its options are "Personal: Only me" (checked and greyed), "Organization: Default", "Workspace: All" and "Workspace: Admins only". The grey box of the owner row sits above the list and covers the start of the last option. | PASS |
| `connection-cells-share-saved-light.png` | The share is saved. | Toast "Access policy saved." The panel of the server with a key reads "Workspace: All". The recommendation line is gone. The other panel is unchanged. | PASS |
| `connection-cells-share-read-back-light.png` | The saved share reads back after a new page load. | After a reload, the same panel still reads "Workspace: All", with no recommendation line. | PASS |
| `connection-cells-share-read-back-dark.png` | Same, dark palette. | Same, dark. | PASS |
| `connection-cells-shared-reading-light.png` | The shared reading. | The same capture as the one-panel picture after the delete: the shared connection alone, reading "Workspace: All". | PASS |
| `connection-cells-shared-reading-dark.png` | Same, dark palette. | Same, dark. | PASS |

Not reached: the locked reading. The MCP Servers connector recommends a scope. It does not set a ceiling, so no locked picker can show on a connection made on this page. The scope line of these panels shows the recommendation form instead.

## Notes on every picture

- The round "N" button at the bottom right is the indicator of the development build. It is not part of the product page.
- To the right of the tab labels, the line under the tab strip shows as two thin lines in the light palette.
