# Per-scope assignment pages: real pages, both palettes

Head commit: `34f2f54b4c60757543e61811f8f2724a86517118`.

Every frame comes from one production build of that head, served by the prebuilt
standalone server and started the way the repository's own end-to-end workflow
starts it (static and public copied next to `server.js`, the environment file
loaded into the shell, the development-mode extension tree switched on). No
development server took part. Two server lives, both on a loopback port of their
own, with a dedicated database and a dedicated cache.

Every page was reached through the product: the scope page, its Agents or
Assistants tab, then a card's **Settings** text link. The link's address was
recorded the first time on each scope, and only then was a direct address used to
switch the palette or the pane. The palette was set on the page itself and read
back from the document's own class before each capture.

Account names and electronic mail addresses carry a solid block, applied before
the capture. The two-letter initials in the account bubble are left as they are:
they are neither a name nor an address.

## What was seeded

Three accounts, all obviously fake. The first registered account is the platform
administrator and the owner of the one organization; a second account is an
administrator of that organization, of the one team and of the one project; a
third account is an ordinary member of the organization, a plain member of the
team and holds write on the project.

Two agent packages were uploaded and installed at the organization through the
product's own upload screen: one that declares a context slot taking a brand
voice, and one that declares no context slots. The platform's own bundled agents,
skills and assistant were already present from the boot.

One document was uploaded on the Artifacts surface during this round. The product
filed it as a Markdown artifact. No artifact of the brand voice kind exists on
this boot; see the report for why.

## The frames

| File | Requires | Shows | Verdict |
|------|----------|-------|---------|
| `scope-workspace-agents-tab-light.png` | The workspace Agents tab with cards, each carrying a Settings text link left of More details | The tab with its cards and Settings links | pass (recorded, not counted) |
| `scope-personal-agents-tab-light.png` | The personal Agents tab with cards and their Settings links | The tab, including the two uploaded packages | pass (recorded, not counted) |
| `cell1-personal-skills-before-light.png` | Kicker PERSONAL, the agent's name, its byline, the Skills and Artifacts strip with Skills selected, the limits line, the labelled chooser, the zero count hint | All of it, in the light palette | pass |
| `cell1-personal-skills-before-dark.png` | The same, dark palette | The same, dark | pass |
| `cell1-personal-skills-two-chosen-light.png` | Two rows with their state pills and bins, the hint reading two of five | Two rows, each two lines, an Active pill and a bin, the hint | pass |
| `cell1-personal-skills-five-chosen-light.png` | The field greyed, the hint reading five of five and what to do about it | The greyed field, the hint, five rows, no hairline after the last row | pass |
| `cell1-skills-chooser-no-matches-light.png` | The chooser's empty result, plainly stated and not an outage | The list reading No matches. | pass (recorded, not counted) |
| `cell2-personal-artifacts-before-light.png` | Context artifacts, the intro, the group and its takes line, the labelled chooser, the untouched hint | All of it | pass |
| `cell2-personal-artifacts-before-dark.png` | The same, dark palette | The same, dark | pass |
| `cell2-personal-artifacts-chooser-no-matches-light.png` | The chooser narrowed to the slot's own kind | A search of the scope's one stored artifact, which is of another kind, returning No matches. | pass (recorded, not counted) |
| `cell3-personal-artifacts-no-slots-light.png` | The empty state for an agent that declares no slots, with its way back to Skills | The titled empty state and the Go to Skills action | pass |
| `cell3-personal-artifacts-no-slots-dark.png` | The same, dark palette | The same, dark | pass |
| `cell7-workspace-admin-groups-light.png` | The workspace page as the platform administrator: one group per scope the reader belongs to, each with its own chooser and hint | Five groups: workspace, personal, the organization, the team and the project | pass |
| `cell7-workspace-admin-groups-dark.png` | The same, dark palette | The same, dark | pass |
| `cell7-workspace-admin-chooser-searching-light.png` | The chooser open and searching, as a single row that is not a result | The list in flight | pass (recorded, not counted) |
| `cell7-workspace-admin-after-one-skill-light.png` | One skill chosen at the workspace group, saved at once | The workspace group with one row and the hint reading one of five | pass |
| `cell7-workspace-member-groups-light.png` | As an ordinary member: only the personal group writable, the others readable with their own reason | Workspace, the organization, the team and the project each read-only with their reason; personal writable | pass |
| `cell7-workspace-member-groups-dark.png` | The same, dark palette | The same, dark | pass |
| `cell8-workspace-assistant-skills-light.png` | An assistant's page: no pane strip, the Skills pane alone, its chooser labelled for an assistant | No strip and the Skills pane alone, but every group read-only and no chooser | **fail** (see the report, defect two) |
| `cell8-workspace-assistant-skills-dark.png` | The same, dark palette | The same, dark | **fail** |
| `cell8-workspace-assistant-artifacts-address-shows-skills-light.png` | The artifacts address on an assistant shows the same Skills page | The same page, no strip | pass on the address rule, fail on the pane's own state |
| `cell8-workspace-assistant-artifacts-address-shows-skills-dark.png` | The same, dark palette | The same, dark | pass on the address rule, fail on the pane's own state |
| `observation-workspace-platform-agent-manifest-unreadable-light.png` | Recorded only | A bundled agent's Artifacts pane on a production runtime, reporting that the manifest could not be read | recorded |
| `observation-workspace-platform-agent-manifest-unreadable-dark.png` | Recorded only | The same, dark | recorded |
| `observation-workspace-slotless-agent-manifest-unreadable-light.png` | Recorded only | The same, on a bundled agent that declares no slots | recorded |
| `observation-workspace-slotless-agent-manifest-unreadable-dark.png` | Recorded only | The same, dark | recorded |

## Not taken

The organization, team and project assignment pages were not reachable on this
boot, so their twelve counted frames are absent. The reason is in the report.
