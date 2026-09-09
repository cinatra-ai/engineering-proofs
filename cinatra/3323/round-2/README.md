# Second proof round — the Upload Extension screen and the install scope (issue 3204, leg 3)

Pull request head proven: `6791172ab6d1aba28ed0228f164111dc8ea28af2`.

Every frame is the whole browser window at 1440x960 css pixels, device pixel ratio 1, no crop.
Both palettes come from the app's own theme control. The round ran on a development boot per the
2026-09-03 ruling; the framework's own development indicator is hidden through the framework's own
means and proven on pixels — the bottom-right 300 by 300 region reads a single flat page value on
every frame (240.71 in light, 6.45 in dark, minimum equal to maximum), so the floor is unoccluded
everywhere. The topbar's development-only wrench is that road's artefact and is counted against
nothing.

Both sessions were minted by the repository's own extensions-upload harness: the walk organization,
which holds no GitHub connection of its own, and a second session in the organization that holds
the connection. No cell of this screen draws an agent run: every cell is `[no run]`.

| frame | cell | palette | what it shows | verdict |
|---|---|---|---|---|
| cell1-file-artifact-light.png | CELL1 | light | the File tab with an artifact archive read: kind chip `Artifact`, the package name and version, the content digest, and the store's install panel with `Workspace: All` preselected, Cancel and Install now | shows the state |
| cell1-file-artifact-dark.png | CELL1 | dark | the same state in dark | shows the state |
| cell2-github-resolved-light.png | CELL2 | light | the GitHub tab with a repository resolved through the real connection: `pinned at fcef3294624e31eaa64e6af42a64ea8ae1f7de83`, kind chip `Skill`, the same install panel | shows the state |
| cell2-github-resolved-dark.png | CELL2 | dark | the same state in dark | shows the state |
| cell3-github-precondition-no-connection-light.png | CELL3 | light | the GitHub tab in an organization with no usable connection: `There is no usable GitHub connection`, the line naming where it is fixed, and Continue disabled | shows the state |
| cell3-github-precondition-no-connection-dark.png | CELL3 | dark | the same state in dark | shows the state |
| cell4-agent-installed-listed-in-agents-light.png | CELL4 | light | a supplied agent package installed at the chosen scope and then its own row in the agents listing, searched by the name it installed under; the toast was dismissed first so the listing alone carries the evidence | shows the state |
| cell4-agent-installed-listed-in-agents-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-skill-installed-observed-light.png | CELL4 | light | a supplied skill package installed at the chosen scope and then read as its own row in the skills catalog | shows the state |
| cell4-skill-installed-observed-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-connector-refused-light.png | CELL4 | light | a supplied connector package: the per-kind execution boundary refuses it by name through the toast surface and the panel keeps `Workspace: All` exactly as it was left | shows the state |
| cell4-connector-refused-dark.png | CELL4 | dark | the same state in dark | shows the state |
| cell4-artifact-installed-extensions-listing-setup-gated-light.png | CELL4 | light | the installed-extensions listing — the surface the artifact kind is promised on — gated by an instance-setup notice on this boot | shows why the observable could not be reached |
| cell4-artifact-installed-extensions-listing-setup-gated-dark.png | CELL4 | dark | the same, in dark | shows why the observable could not be reached |
| cell4-artifact-area-no-object-of-the-type-light.png | CELL4 | light | the artifacts area after the install: the type filter offers only `Type: All` and the area holds no object of the installed type | shows why the observable could not be reached |
| cell4-artifact-area-no-object-of-the-type-dark.png | CELL4 | dark | the same, in dark | shows why the observable could not be reached |
| cell5-refusal-retired-kind-light.png | CELL5 | light | an archive declaring the retired `workflow` kind refused by name through the toast surface; no install panel is drawn and nothing is written | shows the state |
| cell5-refusal-retired-kind-dark.png | CELL5 | dark | the same state in dark | shows the state |

## What this round fixed against the previous one

* CELL3 was NOT CAPTURED before. It is captured now: the precondition is read per organization, so
  the walk organization states `There is no usable GitHub connection` with Continue disabled while
  the connected organization still resolves a repository for CELL2. One instance, both halves.
* CELL4's agent observable did not exist before — the listing did not carry the package. It does
  now: one row, one match, the toast dismissed before the shutter.
* The connector refusal left a row behind before. It leaves none now: zero rows for this round's
  connector packages, against two rows left by the previous round.

## What could not be shot, and why

* CELL3's second precondition state, `no owning connector`. That state needs the GitHub connector
  itself to be inactive on the whole instance, which would destroy the only connection CELL2 is
  measurable through, and the screen where a connector is deactivated is itself gated by the
  instance-setup notice on this boot. Reported as NOT CAPTURED rather than staged.
* CELL4's artifact observable, `an object of that type`. Both surfaces are shown and both are
  blocked here: the installed-extensions listing is gated by the instance-setup notice, and the
  artifacts area offers no type for the installed package and holds no object of it. The install
  itself completed — the row is `kind=artifact, status=active, owner_level=workspace`.

## Frame integrity

Four CELL4 frames were shot, read, and then DELETED rather than renamed: they were named for the
package being observed where its kind lives, but on the pixels the name appeared only inside the
install toast. The agent state was re-shot under a new name with the toast dismissed first; the
artifact state was replaced by the two frames that name what actually blocks it. One readback
picture of the connector setup page was deleted because that page renders an OAuth client
identifier in clear text; the readback is kept in text instead. Every deletion is recorded in
`dom-readings.jsonl`, and no frame file was overwritten after its reading was written.
