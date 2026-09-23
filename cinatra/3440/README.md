# Real-page pictures for pull request 3440: the Sharing tab

Head commit: 4d522f5c2ef7839d4b24aedc8cefa01f4b0580fe

All four frames come from a development boot of this exact head. The checkout did not change between the boot and the last frame.

Drawing: the Sharing tab in section II of the connectors drawing. The copy used for the grade has the same content hash as the one that the branch's conformance manifest pins.

## Files

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `sharing-tab-app-page-mcp-servers-light.png` | CELL1, light: the Sharing tab for one connection on a connector that recommends a scope. The tab strip, the heading and intro line, one connection row, the permissions card with the Access picker, the recommendation line, the helper line, Ownership with its search field and helper, the owner row with a lock, one right-aligned Save changes. No roll-up card for one connection. | Tabs Setup, Sharing (selected), Help. "Connection sharing" and the intro line. One row: the connection name and the mono line `externalMcp`, with no badge and no action. The card: Access, the picker on "Personal: Only me", the recommendation line, "Choose who can use this connection.", Ownership, "Search by name or email…", the owners helper, one owner row with a lock in place of the remove button, Save changes at the right edge. No roll-up card. | pass |
| `sharing-tab-app-page-mcp-servers-dark.png` | CELL1, dark: the same, in the dark palette | The same parts, in the dark palette | pass |
| `sharing-tab-app-page-mcp-servers-picker-open-light.png` | CELL1, light: the Access picker open. Prefixed rows ordered narrow to broad, a checkbox at the start of each row, a hairline between scope groups, the floor row checked and not selectable. | Personal: Only me (checked and muted), Organization: Default, Workspace: All, Workspace: Admins only. Two hairlines divide the three groups. | pass |
| `sharing-tab-app-page-mcp-servers-picker-open-dark.png` | CELL1, dark: the same open picker, in the dark palette | The same rows and hairlines, in the dark palette | pass |

CELL2 has no file. It asks for the same tab on a connector that draws its own setup page. At this head, no such connector uses the shared tab. Each one adopts the tab in its own repository after this pull request merges (issue 3385, item 2).

## How each page was reached

1. A new development database. An obviously fake account signed up as the first user and thus became the platform admin.
2. The connection service ran beside the app, so that a server added with an API key gets a stored connection.
3. One MCP server was added through the product's own form: the Connectors page, the MCP Servers connector, the Setup tab. Label "Lane throwaway server", Server URL a throwaway local server, API key a made-up token (not a credential; it is in no frame), Scope "Personal (only me)".
4. Each frame: the Connectors page (the page that Connectors in the sidebar opens), then the MCP Servers card, then the Sharing tab.
5. The palette was set before the page loaded. The root class of the page was then read back: `cinatra` for light, `dark` for dark.
6. The picker frames: one click on the Access picker opened it.

## Masking

Solid grey blocks cover the account name and the e-mail address before each capture: in the sidebar footer and in the owner row. The avatar initials stay.

## Seen, not counted against this change

- A lock glyph stands in front of the recommendation line. The drawing puts the lock only on the ceiling line (issue 3454).
- The picker reads "Personal: Only me" on this new connection. Issue 3408 asks for the recommended scope to be preselected. The recommendation line itself shows.
- The tab strip draws two thin navy rules to the right of the tabs, in both palettes. This change does not touch the tab strip.
- The framework's development indicator (bottom right) and the wrench in the top bar show only on a development boot.
- The ceiling line with its lock does not apply here: the MCP Servers connector recommends a scope and sets no ceiling. No shipped connector with a ceiling can hold a real connection on a development installation.
