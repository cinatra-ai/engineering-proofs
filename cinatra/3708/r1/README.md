# Visual proof: the Sharing tab with two saved connections

These frames come from a production build of the change at commit
`c25afc7260912ab7d5f1aaf632f3a4de458281fb`. The build was started the way the
repository's end-to-end workflow starts it: the compiled standalone server,
with the static files and the public files copied beside it, reading the same
settings file the suites read. No development server ran, and nothing was
rebuilt for these pictures.

The account is the first account the instance registered, so it holds the
platform administrator role. Its organization is the Default organization. Two
external servers were registered through the connector's own Setup form, each
with a made up address that never has to answer. Both belong to the same
person, so that person holds two saved connections on this one connector page.

Names, initials and e-mail addresses are painted over with a plain grey block.
The palette of every frame was read off the `<html>` class in the same second
the frame was written: the light frames carry the product's light theme class,
and the dark frame carries the dark one.

## Frames

| File | Palette | What it shows |
| --- | --- | --- |
| `cell1-sharing-two-connections-light.png` | light | Two connection panels, each with its identity row over its access picker and its ownership card. No roll-up card. The tab strip reads Setup, Sharing, Help. |
| `cell1-sharing-two-connections-dark.png` | dark | The same page and the same state in the dark palette. |
| `cell2-sharing-one-connection-light.png` | light | The control: the same page after the first server was saved and before the second. One panel, no roll-up card. |
| `recorded-design-fixtures-rollup-light.png` | light | Recorded, not counted. The internal conformance fixtures route still draws the roll-up card above its two panels, because that mount states the many connections shape. |

## Readings taken with each frame

| Frame | Roll-up cards | Panels ready | Identity rows | Tab strip |
| --- | --- | --- | --- | --- |
| Two connections, light | 0 | 2 | 2 | Setup, Sharing, Help |
| Two connections, dark | 0 | 2 | 2 | Setup, Sharing, Help |
| One connection, light | 0 | 1 | 1 | Setup, Sharing, Help |
| Fixtures route, light | 1, reading "2 Connected" | 2 below the card | 2 | not applicable |

A frame with a roll-up card above the panels, a Connections tab in the strip,
or fewer than two panels would be a defect. None of the counted frames carries
one.

## One note on the seeds

The Setup form offers an optional key field. On this instance the connection
service that stores a key is not configured, so the product refuses a key and
says so on the page itself: register only servers that need no authentication.
The two servers were therefore saved without a key, which is the product's own
road here. The connection identity rows that carry the Sharing tab's panels are
written either way, so the state under test is the intended one.
