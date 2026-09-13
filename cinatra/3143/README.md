# Proof round 17 — artifact displays (media byte road)

Head under proof: e129e53c413966a5a63022ab5070eae3d0cdb791

All frames come from one development boot of the product, signed in through the product's own
sign-in page as the boot's administrator account. The account band in the sidebar footer is
painted over in every frame. The framework's development indicator is switched off through the
framework's own route before every shutter. The wrench control in the topbar is the development
boot's own artefact and belongs to no cell.

The run: the Blog Idea Generator agent was dispatched fresh through its own Run-agent wizard on
this boot and completed; it filed five blog ideas and one JSON list artifact. Every frame below
shows a real page of that run's output, reached through the product's own navigation.

| frame | cell | page | theme |
| --- | --- | --- | --- |
| cell1-artifacts-list-light.png | 1 | Artifacts list, the run's ideas as separate rows | light |
| cell2-idea-reproducible-builds-light.png | 2 | one idea on its own artifact page | light |
| cell2-idea-reproducible-builds-dark.png | 2 | one idea on its own artifact page | dark |
| cell3-json-list-light.png | 3 (observation) | the run's JSON list artifact page | light |
| cell3-json-list-dark.png | 3 (observation) | the run's JSON list artifact page | dark |

measurements.json carries, per frame: sha256, byte size, pixel size, mean luminance, the content
region's luminance, the state the frame shows, the palette, the URL and the breadcrumb read at
the shutter. dom-readings.jsonl carries one appended reading per shutter.

Cell 2 reading: exactly one idea title is present on the page; each of the other four idea titles
the run produced is absent from the page.

Observation on cell 3, not counted: long JSON row values run past the right edge of the value
tree instead of wrapping.
