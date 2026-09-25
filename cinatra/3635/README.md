# Workspace Dashboards tab: picture proof for pull request 3635

Head commit: `cb45a853fc06e24fe134049fa13692af2bfb5d7d` (branch `feat/2811-workspace-dashboards`).
Every frame comes from the running application at that commit. No component render, no fixture route.

All frames are real pages, reached through the product's own navigation: the sidebar entry
**Workspace**, the page's tab strip, the **Add dashboard** popup, and each row's **Open**.
Viewport 1440 by 950. The palette is set in browser storage and verified on the page's root
element before each capture: `cinatra` for light, `dark` for dark.

**Painted areas.** A solid block covers every account name and e-mail address before capture.
The blocks are drawn over the sidebar account chip. Nothing else is altered.

## What was seeded, and how

| Seed | Road taken |
|---|---|
| First account (platform administrator) | The product's own first-run account form. The first account to register becomes the platform administrator. |
| Instance display name and namespace | **Not set.** The product's naming step refuses on this installation (see the report). The Overview surface falls back to naming the scope. |
| Sign-ups on, then off | Configuration, Access control, the "Allow new sign-ups" switch. Turned on before the second account, and off again after it. |
| Second account (a plain member) | The product's `/sign-up` form, in a second browser session. |
| Team "Support" in the Default organization | The product's Teams area, "New team". The administrator is its only member. |
| Team dashboard "Support load — weekly" | A direct row insert. The product has **no form** that creates a dashboard homed in a team: the team tab's Add popup offers the reference section alone. Recorded in the report. |
| Workspace dashboard "Pipeline health — Q3" | The workspace Add popup, "Create new". |
| The reference on the workspace tab | The workspace Add popup, its reference section, "Add". |
| The everyone-grant | The switch on the reference row, set by the platform administrator. |
| Database shape | None needed by hand. The boot ran the whole core migration chain for real, through `core__0108`, into the application schema. Checked after the boot: the dashboards organization column is nullable, the links rule admits `workspace`, both workspace rules and the three grant columns are present. |

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `workspace-dashboards-landing-light.png` | The workspace page opens on Dashboards, a five-entry tab strip with no Settings, the caption, the non-removable Overview first, a created row, no Remove on either. | Exactly that, in light. | pass |
| `workspace-dashboards-landing-dark.png` | The same in dark. | Exactly that, in dark. | pass |
| `workspace-add-popup-reference-section-light.png` | One Add popup with a reference section offering at least one candidate the curator can already open, naming its home. | "Create new" and "Reference an existing dashboard" with the candidate "Support load — weekly", noted as homed in Team: Support, and its Add control. | pass for the cell; two recorded points (section wording, missing catalog section) |
| `workspace-add-popup-reference-section-dark.png` | The same in dark. | The same, in dark. | pass for the cell; same two recorded points |
| `workspace-listing-remove-light.png` | A referenced listing carries Remove; a homed row never does. | The referenced row carries Remove and Open; Overview and the created row carry Open alone. No badge says which row is which. | pass |
| `workspace-listing-remove-dark.png` | The same in dark. | The same, in dark. | pass |
| `workspace-everyone-grant-administrator-switch-light.png` | The platform administrator can set the mark, and reads it once set. | "Visible to everyone" with the switch on, beside Remove and Open. | pass |
| `workspace-everyone-grant-administrator-switch-dark.png` | The same in dark. | The same, in dark. | pass |
| `workspace-everyone-grant-viewer-row-light.png` | A member who is not a platform administrator reads the mark with the control muted, disabled, and the reason named; no Remove. | The row, the mark, a disabled switch, the reason sentence, Open alone. | pass |
| `workspace-everyone-grant-viewer-row-dark.png` | The same in dark. | The same, in dark. | pass |
| `workspace-everyone-grant-viewer-reading-light.png` | The same member opens the referenced dashboard and reads it, with no write control. | The dashboard at its own canonical page, its name, its home chip, and no Edit, Save, Add, Remove or Delete. | pass |
| `workspace-everyone-grant-viewer-reading-dark.png` | The same in dark. | The same, in dark. | pass |
| `workspace-viewer-without-grant-no-row-light.png` | Recorded. Before the grant, the same member sees no row for that dashboard, not a locked one. | Their own Overview alone. The referenced dashboard is absent, and its name is nowhere on the page. | pass |
| `workspace-overview-surface-light.png` | Recorded. The Overview's own page, reached by its Open control. | "404 — Page not found". | **fail** |
| `workspace-homed-dashboard-surface-light.png` | Recorded. The created workspace dashboard's own page, reached by its Open control. | The page, with the trail Workspace, Dashboards, and the dashboard's name. | pass |

## Result

Counted: four cells, eight of eight counted frames pass.
Recorded: one failure. The Overview row's **Open** leads to "404 — Page not found", while the
created workspace dashboard's Open on the same page works. The report carries the evidence.
