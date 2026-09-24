# Real page pictures, round 4

Head: `3d87c9bfb86528b62558cbef38264da3f5019db9`.

Every frame comes from a production build of that head, started the way the
repository's own end to end workflow starts it. No development server ran. The
pages were reached through the product's own navigation: the sidebar's
Connectors page, the MCP Servers card, then the connector's Setup and Sharing
tabs.

Every server was registered on the Setup form. The second server's key is a made
up value. It is in no frame and in no file here. Account names, the address and
the initials are covered with solid grey boxes before each capture. The palette
of every frame was read from the page root class before the capture: light is
`cinatra`, dark is `dark`.

Eleven frames. Ten are counted. One, the Setup tab, is recorded only, so the
round shows where the servers came from.

This round exists to prove that the fourth fix leg, which makes an identity
follow the write that stands, refuses a create over another person's live
identity, and revokes a stored credential on the host delete, changed no drawn
state. It did not: all six states read exactly as they did at the two previous
heads.

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `sharing-tab-before-any-server-empty-light.png` | Before any server, the Sharing tab carries no panel. | Empty tab body, no sharing section, no panel, no roll-up. Page reading: panel count 0, panel states `[]`. | pass |
| `sharing-tab-before-any-server-empty-dark.png` | The same in the dark palette. | The same, root class `dark`. | pass |
| `sharing-tab-keyless-server-panel-light.png` | The server registered with the key field blank has exactly one panel. | One panel. Its row carries the connection name and the connector line and nothing else. Under it the access card with its picker reading "Personal: Only me", its helper line, then the ownership card with the search field, its helper line, the connecting person's row with a lock in place of a remove button, and one right aligned Save changes. No roll-up. Reading: panel count 1, state `ready`. | pass |
| `sharing-tab-keyless-server-panel-dark.png` | The same in the dark palette. | The same, root class `dark`. | pass |
| `sharing-tab-keyless-and-keyed-servers-two-panels-light.png` | With a second server registered with a key, two panels. | Two panels, one per connection. The roll-up heads them and reads "Connections status, 2 Connected", with no check button and no link away, and the list sits directly beneath it. Reading: panel count 2, states `ready, ready`. | pass |
| `sharing-tab-keyless-and-keyed-servers-two-panels-dark.png` | The same in the dark palette. | The same, root class `dark`. | pass |
| `sharing-tab-after-keyless-server-deleted-one-panel-light.png` | After the keyless server is deleted, one panel, the keyed one. | One panel, naming the keyed connection. No roll-up. Reading: panel count 1, state `ready`. | pass |
| `sharing-tab-after-keyless-server-deleted-one-panel-dark.png` | The same in the dark palette. | The same, root class `dark`. | pass |
| `sharing-tab-keyless-server-registered-again-two-panels-light.png` | The same keyless server registered again, same label and same address, key blank: its panel is back, and it carries a fresh identity, not the retired one raised again. | Two panels. The new keyless panel names a connection the first keyless panel never carried. The roll-up reads "2 Connected". Reading: panel count 2, states `ready, ready`. | pass |
| `sharing-tab-after-second-keyless-deleted-one-panel-light.png` | That second keyless server deleted again: one panel. | One panel, the keyed one. No roll-up. Reading: panel count 1, state `ready`. | pass |
| `setup-tab-registered-servers-light.png` | Recorded only, not counted. | The Setup tab with the registration form and the first registered server in the list, so the round shows where the servers came from. | recorded |

## How each state was reached

The account is the platform administrator, the first account registered through
the product's own account form, with a made up name and address. Every
registration used the Setup form's own default scope, which the form labels
"Personal (only me)".

1. Sidebar Connectors, the MCP Servers card, the Sharing tab. Empty.
2. Setup tab, label "Lane demo server, no key", the loopback address of a
   throwaway server, key field left blank, Add server. Then the Sharing tab.
3. Setup tab, label "Lane demo server, with key", a second loopback address, a
   made up key, Add server. Then the Sharing tab.
4. Setup tab, the delete button of the keyless server, confirm. Then the
   Sharing tab.
5. Setup tab, the same label and the same address as step 2, key blank, Add
   server. Then the Sharing tab.
6. Setup tab, the delete button of that keyless server, confirm. Then the
   Sharing tab.

Each palette was pinned before the page load and read back from the page root
class after it.

## Identities after the last state

One read only query over the connection identities of this connector, after the
last state: three rows, one live. The live one belongs to the keyed server. Both
keyless identities are retired, each under its own name rather than the other
one's, so the registration after the delete brought a fresh identity and not the
retired one raised again. The frame of state 5 shows it, because the panel
heading is that name.

## Things seen and recorded, outside this change

- The panel heading is the internal connection name, not the label typed on the
  Setup form.
- The Setup tab's advisory still says a key is not kept, while the same page
  marks the second server as having one.
- The line under the access picker carries a lock where nothing is locked.
- The Setup tab's connection status card reads disconnected while the Sharing
  roll-up in the same state reads connected.
- In the light palette the rule to the right of the tab strip draws as two thin
  lines.
- The key field of the Setup form shows a row of dots when it is empty. That is
  the field's own hint text, not a stored value.
