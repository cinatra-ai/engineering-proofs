# The markdown editor on the artifact page — Code and Preview, editing in place, the saving indicator

A proof round for cinatra-ai/markdown-artifact#2, shot on a development boot with this package
checked out at the pull request head **5bb8eaf0c77dccb38365837ec24208a33bbf4c8c**. Own cells only,
both palettes through the application's own theme control, whole window at 1440x900, device scale 2.

The artifact is a markdown file uploaded through the product's own upload road on this boot, then
opened on its own page.

## What each cell is graded against — the ratified drawing, quoted

Section V.1, "The markdown display — Code and Preview, and the saving indicator":

> "Markdown is drawn by a display of its own, and that display carries two tabs — Code and Preview.
> Only the active tab's view is shown: Code shows the markdown as it is written — syntax-highlighted,
> never plain text ... Preview renders it. They are never drawn side by side, and there is no third
> reading."

> "They are drawn as tabs — the design system's tab strip (Components § Tabs): labels at 13px sans,
> the inactive one slate, the active one indigo under a 2px indigo underline that meets the header's
> rule. Underline only: never pill tabs, and never a toggle or a segmented control."

> "On the artifact's own page the Code view takes an edit in place: there is no edit mode to enter
> and no Save button to find, and a change is stored as it is made."

> "Beside the tabs — alone with them in the header — sits one indicator with two readings while all
> is well: a spinner from the moment the reader starts editing, and a check once the latest change is
> stored. It is never absent while an edit is in flight, and it never reads as stored before it is."

Section XI, "The displays the fleet adds":

> "A display draws the work and nothing about itself — no renderer chip and no provenance line — the
> mono line names the artifact's own type and revision, never the package that drew it."

And the pull request's own sentences: "Real tablist (aria-selected, aria-controls ...), Code labelled
and Preview labelled, exactly one panel rendered — never both — Code holding editable markdown,
Preview holding the rendered document"; "A change is saved as one new revision with the
spinner-then-check".

## The frames

| file | cell | palette | state it must contain |
|---|---|---|---|
| markdown-cell1-code-active-editable-light.png | CELL1 | light | the tablist with Code and Preview, Code active under a 2px underline, the markdown syntax-highlighted and editable in place, exactly one panel drawn, no Save control |
| markdown-cell1-code-active-editable-dark.png | CELL1 | dark | the same |
| markdown-cell2-preview-active-rendered-light.png | CELL2 | light | Preview active, the rendered document, the Code panel absent, still exactly one panel |
| markdown-cell2-preview-active-rendered-dark.png | CELL2 | dark | the same |
| markdown-cell3a-saving-spinner-light.png | CELL3 | light | one change typed in Code, the saving indicator beside the tabs on its spinner reading |
| markdown-cell3a-saving-spinner-dark.png | CELL3 | dark | the same |
| markdown-cell3b-saved-check-light.png | CELL3 | light | the same indicator on its check reading once the change is stored |
| markdown-cell3b-saved-check-dark.png | CELL3 | dark | the same |
| markdown-cell3c-reloaded-saved-revision-light.png | CELL3 | light | after a page reload the stored change is readable, on a revision that moved |
| markdown-cell3c-reloaded-saved-revision-dark.png | CELL3 | dark | the same |

## The measured readings

CELL1, both palettes — read from the live page, not from the picture:

* two elements with `role="tab"`, labelled `Code` and `Preview`; Code carries
  `aria-selected="true"`, Preview `aria-selected="false"`; each names its panel through
  `aria-controls`.
* `role="tabpanel"` count: **1**. The drawn panel is the Code panel, labelled by the Code tab.
* the code view is a live `textarea`, `readOnly=false`, labelled `Markdown source`; no Save control
  is drawn anywhere on the panel or the page's own header beyond the page's Download.
* the source is syntax coloured from the system's own palette: heading `rgb(54, 78, 129)` in light and
  `rgb(6, 156, 228)` in dark, list markers muted, the code span and the link each in their own token
  colour.
* the display's root carries the artifact's own revision and no package name, no renderer chip and no
  provenance line.

CELL2, both palettes: Preview carries `aria-selected="true"`, Code `aria-selected="false"`;
`role="tabpanel"` count is still **1**, and the drawn panel is the Preview panel — the code editor
element is absent from the page (`null`), so the two readings are never drawn side by side.

CELL3, both palettes:

* on the first keystroke the header grows one `role="status" aria-live="polite"` element with
  `data-saving-indicator="saving"`, the text `Saving...` and a spinning mark; it sits at the end of
  the tab-strip row, beside the tabs, and nothing else joins the header.
* once the change settles, the same element reads `data-saving-indicator="saved"`, the text `Saved`
  and a check mark drawn in the success colour.
* the revision moved with the change: light `08b38bbc-96e9-4602-85d0-79e7bc3307b3` to
  `1ab05f24-fc9e-432c-a919-83420915bc7b`, dark `1ab05f24-...` to
  `f0d6ef2f-2456-4e31-924d-1b3728014178`.
* after a page reload the stored text is what the Code view reads back — the typed line is present in
  the source and the byte size on the page header grew with it (265 to 306 to 346 bytes).

## Frame discipline

Every frame is the whole window at 1440x900, device scale 2 (2880x1800 pixels), the floor beneath the
display unoccluded, and one distinct file name per frame. The framework's development indicator is
disabled through its own persisted preference before the boot and through its own disable call after
it; `measurements.json` records, per frame, the mean luminance of the bottom-right 120x120 region
where that indicator draws: it is flat at the page ground in every frame — 240.71 in light, 6.45 in
dark, minimum equal to maximum. The application's own development-tools control in the page's top bar
is the development boot's own artefact; it is named here once and counted in no cell.

`measurements.json` carries per frame: file name, byte size, pixel size, sha256, and the two
luminance regions.

## Verdicts

| cell | verdict |
|---|---|
| CELL1 light / dark | PASS |
| CELL2 light / dark | PASS |
| CELL3 light / dark (spinner, check, the stored revision after a reload) | PASS |

No departure from the quoted sentences was measured in the cells this pull request owns.
