# Upload Extension screen and install scope panel — proof round

Every frame below was shot in a real browser against a running development boot of the
pull request head, through the product's own controls. Both palettes come from the app's
own theme control. The framework's development indicator is hidden by the framework's own
means and measures 0 by 0 on every frame. The topbar wrench ("Open development tools") is
the development-boot road's own artefact and is not part of any cell.

No cell of this screen dispatches an agent run: every cell is [no run].

## The frames

| Frame | Cell | Palette | What it shows | Verdict |
| --- | --- | --- | --- | --- |
| cell1-file-tab-artifact-archive-resolved-kind-and-scope-panel-light.png | CELL1 | light | The File tab with an artifact package archive read: the resolved kind badge reads Artifact, the package name and content digest are shown, and the store's install panel is mounted on the screen with the picker preselected to Workspace: All and a Cancel / Install now action row. No popup. | pass |
| cell1-file-tab-artifact-archive-resolved-kind-and-scope-panel-dark.png | CELL1 | dark | The same state in the dark palette. | pass |
| cell2-github-tab-repository-resolved-pinned-commit-and-scope-panel-light.png | CELL2 | light | The GitHub tab with a repository resolved through a real GitHub connection: the pinned commit sha is displayed beside the repository, the resolved kind reads Skill, and the same install panel is drawn with the same preselection. | pass |
| cell2-github-tab-repository-resolved-pinned-commit-and-scope-panel-dark.png | CELL2 | dark | The same state in the dark palette. | pass |
| cell3-github-tab-precondition-no-usable-connection-submit-disabled-light.png | CELL3 | light | The GitHub tab in an organization that holds no usable connection: the tab names the precondition in product words and Submit is disabled. | pass |
| cell3-github-tab-precondition-no-usable-connection-submit-disabled-dark.png | CELL3 | dark | The same state in the dark palette. | pass |
| cell4-agent-in-the-agents-listing-at-the-chosen-scope-light.png | CELL4 | light | An agent package installed through the screen at the chosen scope, then seen on the agents listing. | pass |
| cell4-agent-in-the-agents-listing-at-the-chosen-scope-dark.png | CELL4 | dark | The same state in the dark palette. | pass |
| cell4-uploaded-skill-on-the-agent-cards-own-skills-offer-light.png | CELL4 | light | The uploaded skill offered on an installed agent card's own Skills offer, marked Active. | pass |
| cell4-uploaded-skill-on-the-agent-cards-own-skills-offer-dark.png | CELL4 | dark | The same state in the dark palette. | pass |
| cell4-artifact-packs-declared-type-offered-in-the-artifacts-type-picker-light.png | CELL4 | light | The artifacts area's own type picker offering the uploaded pack's declared object type. | pass |
| cell4-artifact-packs-declared-type-offered-in-the-artifacts-type-picker-dark.png | CELL4 | dark | The same state in the dark palette. | pass |
| cell4-artifact-object-rendered-under-the-packs-declared-type-light.png | CELL4 | light | An object filed under the pack's declared type, with the area's own type filter carrying the pack. | pass |
| cell4-artifact-object-rendered-under-the-packs-declared-type-dark.png | CELL4 | dark | The same state in the dark palette. | pass |
| cell4-connector-configuration-surface-after-install-light.png | CELL4 | light | A conforming connector package that declares its access scope, installed through the screen: its own configuration surface renders with the declared field and the connection-status card. | pass |
| cell4-connector-configuration-surface-after-install-dark.png | CELL4 | dark | The same state in the dark palette. | pass |
| cell4-connector-without-access-scope-refused-on-the-toast-surface-light.png | CELL4 | light | A connector package that declares no access scope is refused in one product sentence on the toast surface, fully inside the window, with the panel unchanged and the selection kept at Workspace: All. No inline repeat in the file card. | pass |
| cell4-connector-without-access-scope-refused-on-the-toast-surface-dark.png | CELL4 | dark | The same state in the dark palette. | pass |
| cell5-retired-kind-archive-refused-on-the-toast-surface-light.png | CELL5 | light | An archive declaring the retired kind is refused by name on the toast surface, fully inside the window; the install panel never draws and nothing is written. No inline repeat in the file card. | pass |
| cell5-retired-kind-archive-refused-on-the-toast-surface-dark.png | CELL5 | dark | The same state in the dark palette. | pass |

## Not shot

CELL3's second precondition state — "no owning connector" — was not shot. Reaching it needs the
GitHub connector inactive across the whole instance, which would remove the connection CELL2 is
shot on. It stays named here rather than substituted.

## Readings

Every frame carries a reading taken at the shutter in `dom-readings.jsonl`, and
`measurements.json` carries each file's digest, size, pixel size, mean luminance and the
luminance of the region the cell names.
