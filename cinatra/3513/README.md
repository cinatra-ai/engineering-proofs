# Upload Extension — the repository-link road, ninth proof round

Six counted frames, three cells, both palettes, all shot fresh at the candidate head
`b37c2f37b24dfb806c7ed566bde4c6cc100e9e90` on a development boot, through the product's own
navigation (Extensions page, then its Upload control). No agent run was dispatched: all three
cells are `[no run]`.

The fixture is the public repository `cinatra-ai/web-research-skill`, typed as the bare link
`https://github.com/cinatra-ai/web-research-skill` with no branch, tag or commit.

## The frames

| file | cell | state | palette |
| --- | --- | --- | --- |
| `cell1-github-tab-bare-link-resolved-install-panel-light.png` | 1 | the bare link resolved in place into the install panel, four readings on three rows above the install-for panel | light |
| `cell1-github-tab-bare-link-resolved-install-panel-dark.png` | 1 | the same state | dark |
| `cell2-installed-extensions-page-fixture-skill-card-light.png` | 2 | the installed-extensions list after the completed link-road install, the fixture's card scrolled whole into the window | light |
| `cell2-installed-extensions-page-fixture-skill-card-dark.png` | 2 | the same state | dark |
| `cell3-cancel-closed-the-mounting-typed-link-kept-light.png` | 3 | Cancel closed the mounting back to the choose-a-package state, the selection discarded, the typed link still standing in the field | light |
| `cell3-cancel-closed-the-mounting-typed-link-kept-dark.png` | 3 | the same state | dark |

Two frames beside them are not counted:

  development indicator was switched off through the framework's own route. Both bottom corners
  were looked at and carry no badge; the indicator element measures 0 by 0 in every counted frame
  not a counted frame.
  list, taken immediately after the install completed and before the list had been scrolled to the
  fixture. It does not contain the fixture's card, so it is named for what it actually shows and is
  not the cell's frame.

## The readings

`dom-readings.jsonl` carries one appended reading per shutter: the path, the breadcrumb, the
handles and their text, the picker trigger's text character for character, the resolved panel's own
computed surface, and the tab strip and kind badge readings. `measurements.json` carries each
file's sha256, bytes, pixel size, mean luminance and the luminance of the region the cell requires.

The resolved mounting's root node reads, at this head: a composed separation of 18px above it
(the parent's own 24px column gap less this node's 6px negative top margin, measured at 18px on
the page as well), a 1px top border in the hairline colour with the other three edges at 0, a
corner radius of 0, no background tint of its own, 14px of top padding and a 10px row gap — a top
rule and nothing else, with no second box around it. The one bordered, rounded surface in the
frame is the tab content's own, which the drawings put around this screen's content.

The access-scope picker's closed trigger reads `Workspace: All` — the scope type, a colon, exactly
one space, then the name (code points 87 111 114 107 115 112 97 99 101 58 32 65 108 108). Its
prefix is drawn uppercase by a style rule, not by a re-cased string.

The provenance line reads the proved default branch name `main`, never the stand-in, and the
pinned-commit line reads the single commit the archive was generated from.

Every frame is the whole window; the required region was scrolled into the window before each
shutter and its box recorded with a non-negative height. The account band is painted over in every
counted frame. The wrench control in the topbar is the development boot's own artefact and is not
counted against any cell.
