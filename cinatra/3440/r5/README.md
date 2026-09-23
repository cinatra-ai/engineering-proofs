# Sharing tab proof, round 5

Head commit: `7eb5fe2079207bcb92ea8ca7743ba1d859215708`.

What changed at this head: the shared component now draws the Sharing tab's
permissions card itself, from plain data and four bound actions. Before this
head the app page handed the card in as a ready made piece. The reading is the
same as the earlier round: nothing a person sees may differ.

How the frames were made. The application was built for production and started
the way the repository's own end to end workflow starts it. No development
server ran. One account was registered, and it became the platform
administrator. One server was registered through the MCP Servers connector's
own Setup form, with a made up token in place of an API key; the token appears
in no frame. The page was reached through the product's own navigation:
Connectors, then the MCP Servers card, then the Sharing tab. The palette was
set before the page loaded and read back from the root element's class on every
frame. The account name and e mail address are painted over with solid blocks
before capture.

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `sharing-tab-app-page-mcp-servers-light.png` | The Sharing tab for one connection, light palette: the tab strip with Sharing second, the heading and intro line, one connection row, the permissions card with the Access picker, the recommendation line and the helper line, Ownership with its search field and the locked owner row, one right aligned Save changes, no roll up card | All of it. Root class `cinatra`. The card sits on the surface ground, separate from the connection row. The connection row carries its name and mono line only, with no status badge and no action | pass |
| `sharing-tab-app-page-mcp-servers-dark.png` | The same, dark palette | The same anatomy, dark palette. Root class `dark` | pass |
| `sharing-tab-app-page-mcp-servers-picker-open-light.png` | The Access picker open: the four options in their scope groups, a hairline between the groups, the current value marked | Four options, ordered narrow to broad: Personal Only me, Organization Default, Workspace All, Workspace Admins only. Two hairlines, one between each pair of groups. Only me is ticked, dimmed and not selectable, because it is the floor and the only choice below the rest | pass |
| `sharing-tab-app-page-mcp-servers-picker-open-dark.png` | The same, dark palette | The same four options, the same two hairlines, the same marked value. Root class `dark` | pass |

Recorded on the frames, not counted against this change:

- A small lock stands in front of the recommendation line. The drawing gives
  that lock to the ceiling line only. Tracked as its own issue; unchanged here.
- The picker reads Only me on a connection nobody has touched, although the
  connector recommends the whole workspace. Tracked as its own issue;
  unchanged here.
- Two thin rules run to the right of the tabs instead of one. The tab strip is
  not part of this change, and another change recorded the same thing on
  another page.

Not shown, and why: no installed connector draws its own setup page through
the shared tab yet, so that half of the proof has no page to stand on at this
head. A connector that sets a hard ceiling on its sharing scope cannot hold a
real connection on a development installation, so the ceiling form of the line
under the picker has no reachable state either.
