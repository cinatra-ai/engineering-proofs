# Visual proof, round 3: the connection identity of a keyless MCP server

Head commit: `e46747e76d1bd521532286f335d2921b17025bc3`.

Every frame comes from a production build of that head, started the way the
repository's end to end workflow starts it. No development server ran. The pages
are the real product pages, reached through the product's own navigation:
the sidebar entry Connectors, then the MCP Servers card, then that connector's
Setup and Sharing tabs. Servers were registered and deleted on the Setup form.

The account is the platform administrator, the first account registered through
the product's own account form, with a made up name and address. Grey boxes
cover the account name, the address and the initials in every frame. The key of
the server that has one is a made up value and appears in no frame.

The palette of each frame was checked on the page root class before the capture:
the light frames read `cinatra`, the dark frames read `dark`.

## What each frame requires, shows and proves

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `sharing-tab-before-any-server-empty-light.png` | With no saved connection, the Sharing tab has no panel. | The Sharing tab is open and the area below the tab strip is empty. Page reading: 0 panels. | pass |
| `sharing-tab-before-any-server-empty-dark.png` | The same in the dark palette. | The same, dark. Page reading: 0 panels. | pass |
| `sharing-tab-keyless-server-panel-light.png` | A server registered with the key field left blank has exactly one panel. | One panel, named for the keyless connection, connector line `externalMcp`, an Access card with the picker on Personal, an Ownership card with the search field and the owner row, one Save changes. No roll-up. Page reading: 1 panel, state ready. | pass |
| `sharing-tab-keyless-server-panel-dark.png` | The same in the dark palette. | The same, dark. Page reading: 1 panel, state ready. | pass |
| `sharing-tab-keyless-and-keyed-servers-two-panels-light.png` | After a second server is registered with a key, there are two panels. | Two panels, the keyless one first and the keyed one second, above them a roll-up reading Connections status, 2 Connected. Page reading: 2 panels, both ready. | pass |
| `sharing-tab-keyless-and-keyed-servers-two-panels-dark.png` | The same in the dark palette. | The same, dark. Page reading: 2 panels, both ready. | pass |
| `sharing-tab-after-keyless-server-deleted-one-panel-light.png` | After the keyless server is deleted, one panel is left, the keyed one. | One panel, named for the keyed connection. The roll-up is gone. Page reading: 1 panel, state ready. | pass |
| `sharing-tab-after-keyless-server-deleted-one-panel-dark.png` | The same in the dark palette. | The same, dark. Page reading: 1 panel, state ready. | pass |
| `sharing-tab-keyless-server-registered-again-two-panels-light.png` | The same keyless server registered again, same label and same address, key blank, brings its panel back under a fresh name. | Two panels. The second is named `external-mcp-keyless-9257a52e-3c2a-4f7f-9727-3cc6e462e651`, which is not the first keyless panel's `external-mcp-keyless-27ee2ad6-4106-4783-ad72-f32614d9f0f2`. Page reading: 2 panels, both ready. | pass |
| `sharing-tab-after-second-keyless-deleted-one-panel-light.png` | That second keyless server deleted again leaves one panel. | One panel, the keyed connection. No roll-up. Page reading: 1 panel, state ready. | pass |
| `setup-tab-registered-servers-light.png` | Recorded, not counted: where the servers come from. | The Setup tab with the registered server list, the Label, Server URL, API key and Scope fields, and the Add server button. | recorded |

## How each page was reached

1. Sign in as the administrator account, then the sidebar entry Connectors.
2. The MCP Servers card on that page opens the connector, which lands on its
   Setup tab.
3. The Sharing tab is the second tab of the same connector page.
4. Each server was registered by filling the Label, Server URL and Scope fields
   of the Setup form and pressing Add server. The key field was left blank for
   the keyless registrations and filled with a made up value for the keyed one.
5. Each deletion used the delete button of the row in the registered server list
   and its confirmation.
6. The palette was pinned before each load and read back from the page root
   class before the capture.

## Identity rows after the last state

One read only query over the connection identities of this connector returned
three rows: one live identity, which belongs to the keyed server; and two
retired identities, one for each keyless registration, each under its own name.
The unique index over the live identities therefore holds with no duplicate.
