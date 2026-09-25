# Proof round 3: the workspace Overview opens at its own address

These frames re-shoot one defect for the workspace Dashboards work. Round 1 and round 2 both found
that the Overview row's Open control answered "Page not found". The change has since moved on twice.
This round asks one question: does that row now open its own page?

It does, in both palettes.

## What produced the frames

- **Commit:** `59f710e79a3195a5147ae745038be45a46fe8514`, the branch head at the time of the round.
  Every frame is bound to it. (The branch moved on afterwards; these frames do not cover that.)
- **The build:** a production build of that commit, started the way the repository's own end-to-end
  workflow starts one. The static assets and the public folder were copied into the standalone
  folder, the environment file was sourced, and the standalone server was started once by hand on an
  isolated port. It lived through the whole round: one process, no restart.
- **Not the development server.** No development server ran, and no build ran during the round.

## The database and what was seeded

A fresh, isolated database and cache, created for this round and removed afterwards. The database was
prepared in three steps: the container's own empty database, then the repository's public schema
script, then the authentication migration. The application's own boot then applied the whole core
migration chain, 93 migrations, ending at the workspace-dashboards migration; its precondition check
then read that the schema was current. The shape was read back on its own and holds: the dashboards
organization column is nullable, both workspace shape rules are present, the links rule admits the
workspace kind, and the three workspace grant columns exist.

Seeded through the product, in this order:

1. **The platform administrator.** The first-run account form. The first account to register becomes
   the platform administrator; the store confirms its role. The account is an obvious placeholder.
2. **One workspace dashboard.** The Add popup on the workspace Dashboards tab, "Create new", named
   "Pipeline health Q3".

No second account and no team dashboard: this round settles one question only.

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `workspace-dashboards-landing-light.png` | The row list the Open control came from. | The workspace page open on Dashboards, two rows, Overview first, each with its own Open. | recorded |
| `workspace-overview-open-own-address-light.png` | The Overview row's Open, followed through the product, opens the Overview at its own address for its owner: a page, not the not-found page. | The Overview page, headed "Overview", under the Workspace label, with the trail Workspace, Dashboards, Overview, a Workspace card and the three counts. | pass |
| `workspace-overview-open-own-address-dark.png` | The same rule in the dark palette. | The same page, dark. | pass |
| `workspace-created-dashboard-open-light.png` | The created dashboard's row Open opens that dashboard's own page. | The page, headed "Pipeline health Q3", under the Workspace label. | pass |
| `workspace-created-dashboard-open-dark.png` | The same, dark palette. A companion frame, not asked for. | The same page, dark. | recorded |
| `workspace-overview-reload-found-again-light.png` | The Overview address, loaded once more, is found again, and no second Overview row appears. | The Overview page again, unchanged. A read-only count over the store afterwards reads exactly one Overview row for this person. | pass |

## The addresses and the headings

- **The Overview**, in both palettes. The Open control writes the address escaped, and the browser
  landed on it escaped:
  `/workspace/dashboards/dash%3Aworkspace%3A__workspace__%3Auser%3A<person>%3Aoverview`.
  Written plainly, that is
  `/workspace/dashboards/dash:workspace:__workspace__:user:<person>:overview`.
  Heading: **Overview**.
- **The created dashboard**, in both palettes. Address: `/workspace/dashboards/<plain identifier>`.
  Heading: **Pipeline health Q3**.

The Overview address is the one that failed in both earlier rounds. It carries punctuation, and the
page now reads its address segment decoded before it compares, looks up and checks access. That is the
whole of the difference.

## Two things in the frames that are not this change

- **The Workspace card reads "Name: Workspace".** The first-run naming step refuses on an isolated
  development installation, because that installation carries two credential settings the step treats
  as exclusive. No instance identity was written and none was forged, so the card names the scope
  rather than an instance. Both earlier rounds recorded the same. It is a property of the isolated
  installation.
- **Two short parallel rules sit to the right of the last tab** in the light landing frame. The same
  drawing appears on pages this work does not touch, so it belongs to the shared page shell. Round 1
  recorded it, and another pull request records the same observation.

The created dashboard's page has an empty canvas. A blank dashboard is created empty and nothing was
placed on it; that is the product behaving as asked, not a fault.

## Reading the frames

- **Palette.** Verified on the page's root element class before every capture: `cinatra` for light,
  `dark` for dark, never both. The class was read again on the page the Open control landed on.
- **Identities.** The account name and the e-mail address are covered with a solid block before every
  capture. The address bar is not in the frames; the addresses are quoted above instead. The person
  identifier inside the Overview address is written as `<person>` in this text.
- Every frame is a real page, reached through the product's own navigation: the sidebar, the tab
  strip, the Add popup, and each row's own Open control. No fixture page and no component render.
