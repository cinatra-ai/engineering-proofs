# Proof round — cinatra#3581, round 1 at a35a0477

An installed card draws the plain-text meaning of a markdown description, in both palettes, on a development boot.

Every frame was taken on a running development boot, at 1440x900, through the product's own navigation: the product's own sign-in page, the app shell's topbar Configuration control, the configuration index's Extensions card and its "Installed" link, landing on path /configuration/extensions with no query on its default Active view. No address was typed, no fixtures page was used, and no component test render was involved. The framework's development indicator was switched off through its own route before the first shutter and measured 0 by 0 before each one. The account band is painted over in every frame.

## Frames

| File | Cell | Palette | Counted | What it shows |
| --- | --- | --- | --- | --- |
| `probe-dev-indicator.png` | — | light | no | The throwaway probe frame after the development indicator was switched off: both bottom corners clean. |
| `CELL1-light-installed-extensions-list-whole-window.png` | CELL1 | light | yes | The installed-extensions list on its default Active view, with the card under proof entire in the window (box x=272 y=345 w=1152 h=102). |
| `CELL1-light-card-middle-panel-magnified-crop.png` | CELL1 | light | no | Legibility crop of that card alone. |
| `CELL2-dark-installed-extensions-list-whole-window.png` | CELL2 | dark | yes | The same page, same session, same view, in the dark palette reached by the app's own theme control. |
| `CELL2-dark-card-middle-panel-magnified-crop.png` | CELL2 | dark | no | Legibility crop of that card alone. |

## What was read

The card whose Settings destination reads `/configuration/extensions/settings/agent/@cinatra-ai/lint-policy-agent` draws one description paragraph. In both palettes its full text content equals the plain-text meaning of the stored markdown string, character for character, 551 characters; across all 89 drawn description paragraphs the backtick count is 0, while the stored string for that row carries four inline code-span delimiter pairs; and the paragraph is still one text-only node whose class list is its only attribute, with no child element.

The document root's theme class list carries `cinatra` in CELL1 and `dark` in CELL2, read before each shutter.

`measurements.json` holds each file's sha256, byte count, pixel size, mean luminance and card-region luminance. `dom-readings.jsonl` holds one appended reading per shutter, each naming its frame file.
