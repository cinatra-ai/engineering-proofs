# Round 5 — the closed install road (marketplace listing control), PR 3516 / issue 3494

Head under proof: 1bf4bb91ff6b2d6b503dd9a4230dd242cfa5e171
Surface: the product's own page at /configuration/marketplace, reached by signing in through the
product's sign-in page and walking Configuration to Marketplace. Viewport 1440x900 at device
pixel ratio 2. Palette set through the app's own theme control. No agent run was dispatched.

## What this round photographs

One counted cell, CELL2: an extension listing whose package is not installed, on an installation
whose package registry is NOT connected. The control reads "Install now", is disabled and greyed,
and keeps ONLY its drawn hover title; no reason line is drawn under the control.

## The state of the installation

The installation carries no package-registry configuration of any kind: the environment names no
registry, and the database carries no instance identity row (the whole key list of the metadata
table is connector_config:llm_mcp_access, connector_config:mcp_server, connector_config:nango,
skills_catalog_generation, skills_catalog_rebuild_lease, skills_catalog_rebuild_state — no
instance identity). The storefront therefore resolves the registry as not connected.

Read through the page before the first shutter, signed in as the seal administrator:
  listing cards: 83
  live (enabled) "Install now" controls: 0
  greyed (disabled) "Install now" controls: 78, every one with the drawn title
    "Connect the package registry to install"
  listings already installed: 5
  the not-connected banner: PRESENT — "Installing requires the package registry ... Connect it in
    registry settings to enable Install." with its "Registry settings" control
  the withdrawn reason line under the control: ABSENT everywhere on the page

So the closed install road is this installation's real state, and the greyed control is real,
not arranged.

## Frames

  cell2-closed-road-greyed-install-now-light.png
  cell2-closed-road-greyed-install-now-dark.png

Both at the installation's own origin at /configuration/marketplace, breadcrumb "Configuration Marketplace",
heading "Marketplace". The counted card ("Google Appointment Schedules", a connector listing that
is not installed and reads Compatible) is whole inside the window at 661,386 373x299, its control
at 752,594 87x28 with disabled true, title "Connect the package registry to install", opacity 0.4
and cursor not-allowed. The pointer rested on the control at the shutter so the drawn title is the
live one. No dialog is open, no refusal node is drawn under the card, and the card text carries no
"Connect the package registry to install" line.

Per-file measurements (sha256, bytes, pixels, mean luminance, and the luminance of the card and of
the control region) are in measurements.json; one reading per shutter is in dom-readings.jsonl.

The account band at the foot of the sidebar is painted over in both frames. The framework's own
development indicator was switched off through the framework's own route before the first shutter
and is absent from both readings. The wrench control in the top bar is the development-installation
artefact of this proof round's road and is not counted against any cell.

## Not shot

Nothing else: this round has one counted cell and both of its frames were taken.
