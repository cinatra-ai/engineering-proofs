# Upload Extension — second proof round (pull request 3513, issue 3204 leg 3)

Head under proof: 6340a48760f187ad6df3b67d5688179658da5091. Every frame is a full 1440x900 browser window
(1440x1800 for the two artifact-type frames, where the type picker lists every installed type), shot on a
development boot through the product's own pages. Both palettes are reached with the product's own topbar
theme control. The framework's development indicator is hidden by the framework's own means and proven on
pixels: the bottom-right 300x300 region reads flat page ground on every frame (light 241, dark 7) except the
listing frames, where product cards occupy that corner. No agent run is dispatched in any cell.

## CELL1 — the File tab with an artifact package archive read

- `cell1-file-tab-artifact-scope-panel-light.png` — light — the resolved kind reads Artifact, the package name
  and its content digest are shown, the install panel is mounted on the screen with the picker preselected to
  Workspace: All and the Cancel / Install now row; no popup on the page.
- `cell1-file-tab-artifact-scope-panel-dark.png` — dark — the same state.

## CELL2 — the GitHub tab with a repository resolved

NOT SHOT. This instance holds no GitHub connection in any organization, so the tab meets its precondition in
every session available to the round and no repository can be resolved. The state the tab actually showed is
CELL3's frame pair.

## CELL3 — the GitHub tab's precondition states

- `cell3-github-precondition-no-connection-light.png` — light — "There is no usable GitHub connection": the
  connector is installed but the organization has no usable connection, the copy names the fix and links to
  the connector's settings, and the Continue action is disabled.
- `cell3-github-precondition-no-connection-dark.png` — dark — the same state.
- The second precondition state (no owning connector) is carved out by name: it needs the connector absent
  from the instance, which would remove the state shown above.

## CELL4 — a completed install per kind, observed where the product shows it

- `cell4-agent-installed-observed-light.png` / `-dark.png` — the installed agent package on the agents listing
  at the chosen scope, its card titled by the flow's own name.
- `cell4-skill-installed-observed-light.png` / `-dark.png` — the installed skill package on the skills catalog
  at the chosen scope, its row naming the skill, the extension and the skill id. The deeper observable (the
  skill offered on a package card's own Skills section) is carved out by name: that section is retired on the
  default branch and the per-package assignment page that replaces it is not built yet.
- `cell4-connector-configuration-surface-light.png` / `-dark.png` — the schema-config connector's own
  configuration surface, rendered from the package's declared setup fields, with its connection status card.
- `cell4-connector-refused-toast-light.png` / `-dark.png` — a connector package that declares no access scope
  is refused in one product sentence on the toast surface, fully inside the window, with the panel and its
  Workspace: All selection unchanged and no repeat of the sentence in the file card.
- `cell4-artifact-installed-observed-light.png` / `-dark.png` — the installed artifact package on the
  installed-extensions list.
- `cell4-artifact-declared-type-offered-light.png` / `-dark.png` — the artifact pack's declared object type on
  offer in the artifacts area's own type picker.
- `cell4-artifact-object-filed-under-type-light.png` / `-dark.png` — an object filed under that declared type
  and carried by the area's type filter.

## CELL5 — a refusal on the screen

- `cell5-retired-kind-refusal-toast-light.png` — light — an archive declaring the retired kind is refused by
  name on the toast surface ("a retired extension kind and cannot be installed", the accepted kinds named),
  no install panel is drawn and the file card carries the file only.
- `cell5-retired-kind-refusal-toast-dark.png` — dark — the same state.

## Files beside the frames

- `measurements.json` — per frame: sha256, bytes, pixels, mean luminance, the bottom-right region reading, the
  state it shows and its DOM reading.
- `dom-readings.jsonl` — one appended reading per shutter, in the order they were taken.
