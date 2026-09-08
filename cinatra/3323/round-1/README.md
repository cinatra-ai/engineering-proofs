# Second proof round — Upload Extension screen and install scope (issue 3204, leg 3)

Pull request head proven: `87bf45ea5e8f067a919934c2d45199bf95276ba3`.
Every frame is the whole browser window at 1440x960 css pixels, device pixel ratio 1, no crop.
Both palettes come from the app's own theme preference. The round ran on a development boot per
the 2026-09-03 ruling; the framework's own development indicator is hidden through the framework's
own preference and proven on pixels (the bottom-right 300 by 300 region reads the flat page ground,
240.71 in light and 6.45 in dark, on every frame whose corner is empty page). The topbar's
development-only wrench is that road's artefact and is counted against nothing.

No cell of this screen draws an agent run: every cell is `[no run]`.

| frame | cell | palette | what it shows | verdict |
|---|---|---|---|---|
| cell1-file-artifact-light-b.png | CELL1 | light | File tab, an artifact package archive read: kind chip `Artifact`, package name and version, content digest, and the store's install panel with `Workspace: All` preselected, Cancel and Install now | PASS |
| cell1-file-artifact-dark-b.png | CELL1 | dark | the same state in dark | PASS |
| cell2-github-resolved-light.png | CELL2 | light | GitHub tab, a repository resolved through the instance's real GitHub connection: `pinned at 107d43b8fa22fcf1c852aa923c1a0e7a76408b1d`, kind chip `Agent`, the same install panel | PASS |
| cell2-github-resolved-dark.png | CELL2 | dark | the same state in dark | PASS |
| upload-screen-idle-second-admin-light.png | CELL3 not captured | light | the Upload screen's File tab idle state for a second admin session; the GitHub tab click did not take before the shutter | does NOT show the cell's state — see the note below |
| upload-screen-idle-second-admin-dark.png | CELL3 not captured | dark | the GitHub tab, reached this time, but with neither precondition notice on it | does NOT show the cell's state — see the note below |
| cell4-skill-installed-light.png | CELL4 | light | a supplied skill package installed at the chosen scope, then read as its own row in the skills catalog (the row's own usage column reads not currently used) | PARTIAL |
| cell4-skill-installed-dark.png | CELL4 | dark | the same state in dark | PARTIAL |
| cell4-agent-install-toast-agents-listing-light.png | CELL4 | light | after Install now on a supplied agent package: the screen arrives at the agents listing and the toast names the package; the package is not among the listed agents | FAIL |
| cell4-agent-install-toast-agents-listing-dark.png | CELL4 | dark | the same, in dark | FAIL |
| cell4-agent-search-no-match-dark.png | CELL4 | dark | the agents listing searched for the package installed in this round: no agent matches | FAIL (confirms the miss) |
| cell4-artifact-install-toast-extensions-setup-gated-light.png | CELL4 | light | after Install now on a supplied artifact package: the screen arrives at installed extensions and the toast names the package; that listing is gated by an instance-setup notice here, so the package cannot be read on it | NOT PROVEN |
| cell4-artifact-install-toast-extensions-setup-gated-dark.png | CELL4 | dark | the same, in dark | NOT PROVEN |
| cell4-artifact-area-light.png | CELL4 | light | the artifacts area after that install: no object of the new type exists, so the type renders nothing | NOT PROVEN |
| cell4-artifact-area-dark.png | CELL4 | dark | the same, in dark | NOT PROVEN |
| cell4-connector-refused-light.png | CELL4 | light | a supplied connector package: the per-kind execution boundary refuses it by name through the toast surface and the panel keeps `Workspace: All` exactly as it was left | PASS on the drawn item, configuration surface not reached |
| cell4-connector-refused-dark.png | CELL4 | dark | the same, in dark | PASS on the drawn item, configuration surface not reached |
| cell5-refusal-retired-kind-light.png | CELL5 | light | an archive declaring the retired `workflow` kind refused by name through the toast surface; no install panel is drawn | PASS on behaviour, an inline duplicate of the message is also drawn |
| cell5-refusal-retired-kind-dark.png | CELL5 | dark | the same, in dark | PASS on behaviour, same inline duplicate |

Two frames from the working set are withheld from this proof round on purpose: a readback frame
of the connector setup page (it renders an OAuth client id in clear text, unsafe for a public
repository) and a light-palette agent-search frame whose filter had not applied at the shutter
(it does not show the state it was named for; the dark frame carries that reading instead).

## What could not be shot, and why

* CELL3, both precondition states. This instance holds a real, usable GitHub connection — the one
  CELL2 resolves a repository through. The precondition is read from the connector client for the
  whole instance, not per organization, so neither "no owning connector" nor "a connector with no
  usable connection" exists here; a second admin session in a different organization was tried and
  read the same ready state (the GitHub tab with no precondition notice), which is itself a finding.
  Producing either state means removing the connector or the connection, which would destroy the
  only thing that makes CELL2 measurable and cannot be re-created without a person signing in at
  the provider. Reported as NOT CAPTURED rather than staged.
* CELL4, the agent observable. The install finishes and the toast says the agent can be seen in the
  agents list, but the agents listing does not carry it, and its own search reports no match.
* CELL4, the artifact observable "an object of that type". No object of the new type exists after an
  install, and the installed-extensions listing is gated behind an instance-setup notice here.

## Frame integrity

Two frames were deleted and re-shot under new names because they did not show the state they were
named for: the first CELL1 pair carried the framework's development indicator, and an artifact
type-filter pair caught a control that had not opened. Several CELL4 frames keep their pixels and
were renamed to what they actually show. Every rename and deletion is recorded in the working
directory's own reading log; no frame file was overwritten after its reading was written.
