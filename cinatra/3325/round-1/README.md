# First proof round — the artifact promotion reject re-check (own cells, both palettes)

The round ran on a development boot per the 2026-09-03 ruling. The application's own
topbar development-tools control (the wrench) is that road's artefact; it is named once
here and is never counted against a cell. The framework's own development indicator is
hidden through the framework's own means and is proven hidden on pixels: the bottom-right
300 by 300 css-pixel region reads a FLAT ground on every frame (light 240.71, dark 6.45,
minimum equal to maximum), and the framework portal box reads 0 by 0 in every reading.

Every frame is the whole window at 1440 by 900 css pixels, device scale factor 2
(2880 by 1800 pixels). Nothing occludes the floor. No model was configured or contacted.

## The frames

| file | cell | palette | what it shows | verdict |
|---|---|---|---|---|
| cell1-light-feed-pending-request.png | CELL1 | light | the notifications feed of a platform administrator who is not a member of the organization, with the pending artifact promotion request awaiting a decision | pass |
| cell1-light-reject-refused-not-a-member.png | CELL1 | light | the inline reject refused in place: "You are not a member of this organization, so you cannot decide this promotion request." — the request stays pending | pass |
| cell1-dark-feed-pending-request.png | CELL1 | dark | the same feed and pending request in the dark palette | pass |
| cell1-dark-reject-refused-not-a-member.png | CELL1 | dark | the same refusal, same wording, in the dark palette — the request stays pending | pass |
| cell2-light-feed-pending-request.png | CELL2 | light | the notifications feed of an organization member with write authority, with the same pending request | pass |
| cell2-light-reject-settled-row-cleared.png | CELL2 | light | the inline reject settled: the decided row is gone from the feed and the empty state stands | pass |
| cell2-dark-feed-pending-request.png | CELL2 | dark | the same feed and pending request in the dark palette | pass |
| cell2-dark-reject-settled-row-cleared.png | CELL2 | dark | the same settled reject in the dark palette | pass |

## The rows behind the frames

The promotion request is `proof-req-3272` on the object `proof-artifact-3272`
("Quarterly insight") in the organization Northwind.

* CELL1, both palettes — before: status pending, decided-by empty, decision note empty.
  After the refused reject: status pending, decided-by empty, decision note empty,
  decided-at empty. The object row is unchanged: visibility private, owner level user,
  version 1, the same updated-at instant as before the click.
* CELL2, both palettes — before: status pending. After the reject: status rejected,
  decided-by the organization member who clicked, decision note "Not ready for the
  organization yet.", a fresh decided-at. The object row is again unchanged
  (visibility private, version 1) — a reject never touches the object.

## Honest notes

* The decider of CELL1 is a platform administrator holding no organization membership at
  all while the browsing scope is the organization that holds the request. The product's
  own shell re-scopes a signed-in browser to a membership of its own on every page load,
  so that standing is asserted in the store immediately before the click and read back
  after it: memberships "(none)", active scope the organization that holds the request.
* The first CELL2 light pass ended after its before-shutter, because the driver waited on
  a list element the product removes once the row is decided. No after-frame was taken in
  that pass; the published before-frame is the completed pass's own frame and the readings
  file carries an appended note naming the superseded reading.
* Console errors: zero on all four passes.
