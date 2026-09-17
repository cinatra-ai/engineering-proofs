# Proof round 1 — a failed marketplace install reports on the toast, not in the panel

Four counted frames, two cells in both palettes, all taken on a running development
installation through the product's own navigation: the administrator cog, then
Configuration, then the Marketplace card's own Browse marketplace link, then a real
listing's Install now, then the in-card panel's Install now. Nothing was simulated,
no state was forced and no query string was typed.

The install really fails on this installation because the activation-host allowlist is
derived only from a deployment registry configuration that is absent here, and that
derivation is fail-closed. The failure copy is the classified category copy plus an
opaque diagnostic reference, so the exact sentence is recorded, never predicted.

## Frames

| file | cell | palette |
| --- | --- | --- |
| cell1-install-failure-panel-light.png | CELL1 — the panel at the moment the failure is reported, toast standing | light |
| cell1-install-failure-panel-dark.png | CELL1 | dark |
| cell2-panel-actions-usable-light.png | CELL2 — the same panel a moment later, both actions still usable | light |
| cell2-panel-actions-usable-dark.png | CELL2 | dark |
| probe-dev-indicator.png | throwaway probe, not counted — both bottom corners clean after the framework indicator was switched off through its own route | light |

## Readings

The panel body height is 185 pixels before the press and 185 pixels after the toast, in
both palettes. Its availability state reads ready. No node with a role of alert stands
inside the panel body, and the panel's own text is unchanged across the press. The
submit reads Install now, enabled, with no pending attribute; Cancel reads Cancel,
enabled. The toast text is recorded verbatim in dom-readings.jsonl.

The account band is painted over in every frame. The wrench in the control row is the
development installation's own control and is an artefact of the road, not part of any
cell.

Readings and per-file measurements: dom-readings.jsonl and measurements.json.
