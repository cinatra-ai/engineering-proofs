# Proof round 4: the workspace Add popup's sections and the drawn words

These pictures come from a production build of commit
`af79b68d4cb9f72c04a8d7b785810c5257ba100d`, started the way the repository's own
end-to-end workflow starts one, against a fresh isolated database and cache that
were created for this round and removed afterwards. No code changed. No
development server ran and no build ran.

Every page was reached through the product's own navigation: the sidebar, the
tab strip, each surface's own Add control, and the row controls the surface
draws. Account names and e-mail addresses are covered with a solid block before
capture. The palette is verified on the page's root element class before every
capture: light or dark, never both.

## What was seeded

1. The platform administrator: the first registered account, an obviously fake
   person, created through the first-run account step.
2. A team named Support in the Default organization, created through the Teams
   form, with the administrator as its only member.
3. One team dashboard named "Support load weekly". The product offers no form
   for this: a tenant tab's Add popup deliberately offers only the reference
   path, because the other two paths write a row the tenant tab would never
   list. The row was therefore written directly into the store, which is the
   road the first proof round also took and recorded.
4. A second organization named Second Org, created through the Organizations
   form, so the viewer holds two memberships.

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `workspace-dashboards-landing-light.png` | The workspace landing opens on Dashboards; the caption reads "Your dashboards in the whole workspace" joined by a dash to "and the ones referenced up from the scopes below"; the Overview row; Add dashboard. | Exactly that caption, the Overview row with Open, and the Add dashboard control in the caption row. | pass |
| `workspace-dashboards-landing-dark.png` | The same rule, dark palette. | The same surface, dark. | pass |
| `workspace-add-popup-light.png` | The Add popup, opened from the landing, with its title, its opening line and its sections in the drawn order. | The whole popup in one frame, over the landing it came from. | pass |
| `workspace-add-popup-closeup-light.png` | The same popup, close enough to read every drawn sentence. | Title "Add dashboard"; the opening line; "Create new" with Create and "Homes in the workspace."; "Reference a dashboard from the scopes below" with the candidate row, Reference, and the access helper. | pass |
| `workspace-add-popup-dark.png` | The same popup, dark palette. | The same popup, dark, over the landing. | pass |
| `workspace-add-popup-closeup-dark.png` | The same, close enough to read. | The same sentences, dark. | pass |
| `workspace-listing-referenced-remove-light.png` | The team dashboard, referenced through the popup, is listed on the landing with Remove. | The row "Support load weekly" beside Overview, carrying Remove and Open. | pass |
| `workspace-create-new-name-prompt-closeup-light.png` | Recorded: the field the Create control hands off to. | The prompt "New dashboard", the field named "Dashboard name", Cancel and Create. | recorded |
| `personal-dashboards-tab-no-add-light.png` | Recorded: the Personal Dashboards tab carries no Add control. | The tab, its own caption "The dashboards you own.", and no Add control anywhere on it. | recorded |
| `team-tab-add-picker-light.png` | Recorded: the team tab's own Add picker still reads its own words. | "Add a dashboard to Team: Support" and "Reference an existing dashboard", unchanged. | recorded |

## The installed catalog section

The popup's third section is not in these frames, and that is not a defect. The
section renders only when the read finds at least one row; an empty read
produces no section at all, by a ruling that predates this work, so that an
instance never advertises a capability it does not have.

This instance carries 94 live extension installs. None of them ships a
dashboard template, so the federation finds nothing to offer and the section is
absent. The component that materializes such templates says the same thing
about the current fleet in its own header. The report beside these frames
quotes the store reading.

## Two observations, neither caused by this work

- The first-run naming step refuses on this isolated installation, because it
  holds two credential settings it treats as exclusive and the round needs
  both. No instance identity was written and none was forged.
- Creating the second organization moved the session's active organization to
  it, and the team page then answered not-authorized. The workspace tab kept
  offering that team's dashboard as a reference candidate throughout, which is
  what the workspace vantage is for: it reads from the viewer's memberships, not
  from the active organization.
