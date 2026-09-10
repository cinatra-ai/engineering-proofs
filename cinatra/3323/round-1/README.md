# Proof round — the Upload Extension screen and the install scope (issue 3204, leg 3)

Head proven: `ce06cc269cc5ba72d18255effa97ffda06aa3497`.

Every frame is the whole browser window at 1440x960 css pixels, device pixel ratio 1, no crop.
Both palettes are taken with the product's own theme control in the topbar, and the class the
product itself sets on the root element is read back on every shutter — the previous round drove
the palette from the test harness and shot light twice, which is why the control changed.

The round ran on a development boot. The framework's own development indicator is hidden through
the framework's own means and proven on pixels: the framework's development portal measures 0 by 0
on all thirty readings. The topbar's development-only wrench is that road's artefact and is counted
against nothing.

Every cell of this screen is `[no run]` — nothing here dispatches an agent run.

## The frames

| frame | cell | palette | what it shows | verdict |
|---|---|---|---|---|
| cell1-artifact-light.png | CELL1 | light | the File tab with an artifact package archive read: the resolved kind `Artifact`, the package name and version, the content digest, and the store's install panel preselected to `Workspace: All` with Cancel and Install now, no popup on the page | shows the state |
| cell1-artifact-dark.png | CELL1 | dark | the same state in dark | shows the state |
| cell2-light.png | CELL2 | light | the GitHub tab with a repository resolved through the real connection: the pinned commit displayed in full, the resolved kind `Skill`, and the same install panel with the same preselection | shows the state |
| cell2-dark.png | CELL2 | dark | the same state in dark | shows the state |
| cell3-light.png | CELL3 | light | the GitHub tab in an organization with no usable connection: the precondition named in the product's own words, and the submit action disabled | shows the state |
| cell3-dark.png | CELL3 | dark | the same state in dark | shows the state |
| cell4-agent-light.png | CELL4 | light | the surface the screen hands the admin to after an agent package installs, with the install confirmation on the toast surface | shows the state |
| cell4-agent-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-agent-in-the-agents-listing-searched-by-name-light.png | CELL4 | light | the agents listing filtered to the installed agent's own name; the supplied agent cards are drawn there | shows the state, and names a limit: the card title carries no per-package suffix, so this round's card cannot be singled out from the earlier ones by title alone |
| cell4-agent-in-the-agents-listing-searched-by-name-dark.png | CELL4 | dark | the same, in dark | shows the state, and names the same limit |
| cell4-skill-light.png | CELL4 | light | the skills catalog searched by the package the skill installed under: one row, the skill, its extension, its skill id and its description | shows the state |
| cell4-skill-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-skill-offer-searched-by-the-installed-name-light.png | CELL4 | light | the agent card's OWN Skills offer, searched by the name the skill package installed under: it answers `No matches.` | shows why the observable could not be reached |
| cell4-skill-offer-searched-by-the-installed-name-dark.png | CELL4 | dark | the same, in dark | shows why the observable could not be reached |
| cell4-artifact-light.png | CELL4 | light | the surface the screen hands the admin to after an artifact package installs | shows the state |
| cell4-artifact-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-artifact-row-in-the-extensions-listing-light.png | CELL4 | light | the installed-extensions listing scrolled to the artifact package's own row, with the status filter and the marketplace and upload actions above the list | shows the state |
| cell4-artifact-row-in-the-extensions-listing-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-artifact-settings-light.png | CELL4 | light | the artifact package's own settings address answering: the tile naming the package and the kind `Artifact`, the access-scope permission reading `Workspace: All`, and the marketplace, maintenance and danger-zone regions | shows the state |
| cell4-artifact-settings-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-artifact-object-in-the-artifacts-area-light.png | CELL4 | light | the artifacts area holding an object made through the area's own upload control; the type filter offers `All` and `Text` only, so the object is filed under the built-in text type rather than the type the pack declares | shows the state, and names a departure |
| cell4-artifact-object-in-the-artifacts-area-dark.png | CELL4 | dark | the same state in dark | shows the state, and names the same departure |
| cell4-artifact-object-rendered-light.png | CELL4 | light | that object's own page, rendered: the type badge, the name, the media type and size, and the download action | shows the state |
| cell4-artifact-object-rendered-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-connector-light.png | CELL4 | light | a conforming connector package — one that declares its access scope and its configuration surface — installed through the upload road, and the surface the road hands the admin to: the connector's OWN live configuration page, its declared field drawn and its connection status beside it | shows the state |
| cell4-connector-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-connector-refused-light.png | CELL4 | light | a supplied connector package that declares no configuration: the refusal is one short product sentence on the toast surface, the toast whole inside the window, no repeat inside the file card, and the panel keeping `Workspace: All` exactly as it was left | shows the state |
| cell4-connector-refused-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell5-light.png | CELL5 | light | an archive declaring the retired `workflow` kind refused by name on the toast surface, the toast whole inside the window, no install panel drawn, nothing written | shows the state |
| cell5-dark.png | CELL5 | dark | the same state in dark | shows the state |

## Frames not shot, named

* CELL3's SECOND precondition state — no owning connector — is carved out by name, with its reason:
  it needs the connector inactive across the whole instance, which would break the connection CELL2
  is measured on, and no second organization without an owning connector is reachable on this boot.
* CELL4's agent observable is shot on the agents listing, but the installed card cannot be told
  apart from the earlier supplied ones by its title; the row itself is read back from the store.
* Two frames of the skills offer were shot while the picker was still searching. They were discarded
  rather than kept under a name they did not show, and the offer was shot again once it had settled.

## What the rows say

* All four kinds installed at the scope the panel was left at:
  `agent`, `skill`, `connector`, `artifact`, each recorded active and held at the workspace level.
* Both refusals wrote nothing: the store holds no row for the connector package that declares no
  configuration and none for the retired-kind archive.
* The artifact pack's own object type is claimed and active in the store
  (`claim_kind=dedicated`, `status=active`, generation 1), which is what the leg's post-install
  projection is for; the artifacts area's own type filter nevertheless offers only the built-in
  text type.
* The skill's catalog row exists with its extension recorded, and the skills catalog lists it —
  but it carries no recorded provenance, and the agent card's Skills offer answers `No matches.`
* No agent run was dispatched for any cell.
