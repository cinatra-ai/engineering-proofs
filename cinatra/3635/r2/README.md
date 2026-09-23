# Workspace dashboards, proof round 2

Head this round is bound to: `9dd2b159ebdf286033133c013b41e3131fba24e2`.

The frames come from a production build of that head, started the way the
end-to-end workflow in this repository starts it. No development server ran.
Every page was reached through the product's own navigation: the sidebar entry
Workspace, the tab strip, the Add popup, and each row's own Open control.

This round settles one question alone: does the Overview row's Open open the
Overview at its own address for its owner? It does not. The answer is the same
in both palettes.

## What was seeded

- One account, the platform administrator, registered through the first-run
  account form. The name and the address are invented; both are painted over in
  every frame with a solid block before capture.
- One workspace dashboard, "Pipeline health Q3", created through the Add popup
  on the workspace Dashboards tab, with Create new.
- Nothing else. No second account, no team, no team dashboard.
- The database was fresh. The boot applied the whole core migration chain by
  itself, the workspace dashboards migration included, so no statement was run
  by hand. The shape was read back afterwards and is correct: the dashboards
  organization column is nullable, the links rule admits the workspace kind,
  both workspace rules are present, and the three grant columns exist.

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `workspace-dashboards-landing-light.png` | The workspace page opens on Dashboards and lists the rows an Open comes from. | Two rows, Overview first and "Pipeline health Q3" second, each with Open. | pass (recorded) |
| `workspace-dashboards-landing-dark.png` | The same list in the dark palette. | The same two rows, each with Open. | pass (recorded) |
| `workspace-overview-open-own-address-light.png` | The Overview row's Open opens the Overview at its own address: a page, not the not-found page. | The not-found page. | **fail (counted)** |
| `workspace-overview-open-own-address-dark.png` | The same, dark palette. | The not-found page. | **fail (counted)** |
| `workspace-created-dashboard-open-light.png` | The created dashboard's row Open opens that dashboard's page. | The page, headed "Pipeline health Q3", under the Workspace label. | pass (counted) |
| `workspace-overview-reload-found-again-light.png` | The Overview address, loaded a second time, is found again. | The not-found page. | **fail (counted)** |

Counted frames: 4. Counted defects: 3.

## The addresses and the headings

- The Overview row's Open leads to
  `/workspace/dashboards/dash%3Aworkspace%3A__workspace__%3Auser%3A<person>%3Aoverview`.
  The heading reads "404 - Page not found".
- The created dashboard's Open leads to `/workspace/dashboards/<plain id>`.
  The heading reads "Pipeline health Q3".

## The row count

One read-only query over the store counted the dashboard rows this person owns
after the whole round: two rows, of which exactly one is the Overview. The
find-or-create never made a second Overview row.

## Palette

Each palette was verified on the page's own root element class before capture:
`cinatra` for the light frames, `dark` for the dark frames.
