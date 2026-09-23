# Sharing panels for servers registered with and without a key

Round 2 of the picture proof. Every frame comes from a production build of the
change at commit `ce209eda7d47d73cde93b21f0e9f60321ba1cedc`, started the way the
end to end workflow of this repository starts it. Nothing is a mock, a fixture
page or a component render: each state was made through the product's own
screens, and the pages were reached through the product's own navigation.

How the pages were reached: the sidebar entry for connectors, then the card for
the MCP Servers connector, then that connector's Setup and Sharing tabs. Servers
were registered on the Setup form only. The key of the keyed server is an
obviously fake value; it is in no frame and in no file here. Grey boxes cover the
account name, the address and the initials.

Palette: verified on the class of the page root before each capture, `cinatra`
for light and `dark` for dark. The panel count in the table below is the number
of sharing panels the page itself reports, read from the rendered page.

## Counted frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| sharing-tab-before-any-server-empty-light.png | No server saved yet, so no panel. | The Sharing tab is empty. Panel count 0, no sharing section, no roll-up. | pass |
| sharing-tab-before-any-server-empty-dark.png | The same in dark. | The same. Panel count 0. | pass |
| sharing-tab-keyless-server-panel-light.png | A server registered with the key field blank still has its sharing panel. | Exactly one panel, state `ready`. It carries the connection name and the connector line, the access picker set to personal, the ownership field, the owner row with a lock, and one Save changes button. No roll-up. | pass |
| sharing-tab-keyless-server-panel-dark.png | The same in dark. | The same. Panel count 1, state `ready`. | pass |
| sharing-tab-keyless-and-keyed-servers-two-panels-light.png | A second server, registered with a key, adds a second panel. | Two panels, both state `ready`, one for each server. The roll-up above them reads 2 Connected, with no check button and no link away. | pass |
| sharing-tab-keyless-and-keyed-servers-two-panels-dark.png | The same in dark. | The same. Panel count 2. | pass |
| sharing-tab-after-keyless-server-deleted-one-panel-light.png | Deleting the keyless server takes its panel away and leaves the keyed one. | One panel, the keyed connection. The roll-up is gone. | pass |
| sharing-tab-after-keyless-server-deleted-one-panel-dark.png | The same in dark. | The same. Panel count 1. | pass |
| sharing-tab-keyless-server-registered-again-two-panels-light.png | Registering the same keyless server again, same label and same address, brings a panel back, and it is a fresh identity rather than the old one raised again. | Two panels again, roll-up 2 Connected. The new panel carries a new connection name, different from the name the first keyless panel carried. | pass |
| sharing-tab-after-second-keyless-deleted-one-panel-light.png | Deleting that second keyless server leaves one panel. | One panel, the keyed connection. No roll-up. | pass |

Ten counted frames, ten pass, none left untaken.

## Recorded, not counted

| File | Shows |
|---|---|
| setup-tab-registered-servers-light.png | The Setup tab right after the keyless registration, so the round shows where the servers came from: the registered list, the label field, the address field, the optional key field and the scope selector set to personal. |

## Read back from the store after the last frame

One read only query over the connection identities of this connector, after the
last state:

- the keyed server has one live identity;
- the first keyless identity is retired;
- the second keyless identity, the one the second registration made, is retired
  as well and carries its own name, not the first one's;
- one live identity in total, so no duplicate live row is left behind.

## Notes on what the frames also show

These are outside the change under proof and count against nothing here.

- The panel heading is the internal connection name, not the label typed on the
  Setup form. With two servers a reader cannot tell which panel belongs to which
  server by the heading alone.
- The advisory at the top of the Setup tab still says a key is not kept, while
  the same page marks the keyed server as having one.
- The line under the access picker carries a small lock even where nothing is
  locked. It only states what the connector recommends.
- The connection status card reads disconnected while servers are registered.
- In light, the rule to the right of the tab strip draws as two thin lines.
- The key field on the Setup form shows eight dots when it is empty. That is the
  field's own hint text, not a stored value; it was read from the page to be
  sure.
