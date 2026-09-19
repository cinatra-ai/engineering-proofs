# Proof round frames — artifact pages and the lifecycle review floor

Twelve frames, six cells in light and dark, all taken on a running development
copy of the app through the product's own navigation. The theme is switched with
the app's own theme control between the two frames of each cell. The framework's
development indicator was switched off through the framework's own route before
the first shutter and its box read 0 by 0 at every shutter. The account band is
painted over in every frame.

## Cells

| cell | what it shows | frames |
| --- | --- | --- |
| 1 | artifact page for an uploaded markdown file, drawn by the markdown package's own display | cell1-r5-note-md-light.png, cell1-r5-note-md-dark.png |
| 2 | artifact page for an uploaded JSON file, drawn by the JSON package's own display | cell2-r5-data-json-light.png, cell2-r5-data-json-dark.png |
| 3 | artifact page for an uploaded binary file, drawn by the binary package's own display | cell3-r5-blob-bin-light.png, cell3-r5-blob-bin-dark.png |
| 4 | artifact page for an uploaded plain-text file, drawn by the text package's own display | cell4-r5-plain-txt-light.png, cell4-r5-plain-txt-dark.png |
| 5 | pending review gate on the live run surface: the type-level floor, its diagnostic with the package segment, and the structured-data view beneath it | cell5-review-gate-light.png, cell5-review-gate-dark.png |
| 6 | artifact page generic fallback for an artifact a real run produced: the same structured-data view with its metadata | cell6-fallback-light.png, cell6-fallback-dark.png |

## Readings beside the frames

- `dom-readings.jsonl` — one appended reading per shutter: the path, the
  breadcrumb, the content region's own render-dispatch attribute with its value,
  and the per-cell readings.
- `measurements.json` — per frame: sha256, byte size, pixel size, mean
  luminance and the content region's luminance.

The four uploaded files were written for this proof round and put through the
product's own upload control, its typed banner and the type picker that banner's
link opens; the file was kept as a file on every one of them and no meaning was
asserted. The run behind cells 5 and 6 is one real run dispatched through the
product's own Run-agent road.
