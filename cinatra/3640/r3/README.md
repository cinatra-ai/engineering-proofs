# Proof round 3: the per-scope assignment page

Head: `b4425ce175dceef58b6d4cfcc4da3b9a29e72483`.

Every frame here comes from a PRODUCTION build of that head, served by the prebuilt standalone
server and started the way this repository's own end-to-end workflow starts it, with the
development-mode extension tree switched on. No development server took part.

The database was empty at the start. Everything below was made through the product:

- Three accounts. The first one registered is the platform administrator and the owner of the
  Default organization. Sign-ups were opened in Configuration, the other two accounts registered
  themselves, and sign-ups were closed again.
- One team, Growth: account A is its Admin, account B is a Member.
- One project, Launch, owned by the team: account A has Admin, account B has Write.
- Account A is also an Admin of the Default organization.
- Four agent packages, each built in memory and supplied through the product's own upload screen,
  each installed at the scope its name says: one at the organization with a context slot, one at
  the organization without a slot, one at the team, one at the project. A fifth upload was a
  throwaway used to settle which install target reaches which tab; it is still listed on the team
  tab and appears in no frame here.

Every page was reached the way a person reaches it: the scope page, its Agents or Assistants tab,
the card's Settings link. The address each link landed on is recorded in the round report. Account
names and e-mail addresses are covered with a solid block before each capture. The palette of every
frame was read back off the page's own root element after the capture.

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `cell1-personal-skills-before-light.png` | personal scope, the kicker, the name, the byline, the two-pane strip with Skills chosen, the limits line, the labelled chooser, the zero count hint | all of it, and the strip is the application's own strip | pass |
| `cell1-personal-skills-before-dark.png` | the same in the dark palette | the same | pass |
| `cell7-workspace-admin-groups-light.png` | the workspace page as the administrator: one writable group per scope the reader belongs to | five groups, workspace, personal, organization, team and project, each with its own chooser and hint | pass |
| `cell8-workspace-assistant-skills-light.png` | an assistant's page: no pane strip, the Skills pane alone, every group writable, the chooser labelled for an assistant | no strip, five writable groups, the label "Which skills should this assistant always use?" on each | pass |
| `cell8-workspace-assistant-skills-dark.png` | the same in the dark palette | the same | pass |
| `cell8-workspace-assistant-artifacts-address-shows-skills-light.png` | the artifacts address of an assistant shows the same Skills pane | the same page, the same five groups | pass |
| `cell8-workspace-assistant-after-one-skill-light.png` | one skill chosen at the workspace group saves and is counted | the hint reads one of five, and the chosen skill is listed with its Active pill | pass |
| `cell4-team-admin-writable-light.png` | the team page as a team admin: the kicker names the team, the chooser is offered | kicker "TEAM · GROWTH", the labelled chooser, the zero hint | pass |
| `cell4-team-admin-writable-dark.png` | the same in the dark palette | the same | pass |
| `cell4-team-admin-one-skill-light.png` | a choice at the team scope saves | the hint reads one of five and the row carries its Active pill | pass |
| `cell4-team-member-readonly-light.png` | the same page as a team member: rows readable, no chooser, the team refusal sentence | "Only an admin of this team can change these assignments.", the row without a chooser or a bin | pass |
| `cell4-team-member-readonly-dark.png` | the same in the dark palette | the same | pass |
| `cell5-project-admin-writable-light.png` | the project page as a project admin | kicker "PROJECT · LAUNCH", the labelled chooser, the zero hint | pass |
| `cell5-project-admin-writable-dark.png` | the same in the dark palette | the same | pass |
| `cell5-project-admin-one-skill-light.png` | a choice at the project scope saves | the hint reads one of five and the row carries its Active pill | pass |
| `cell5-project-member-readonly-light.png` | the same page as a member with write access only: rows readable, no chooser, the project refusal sentence | "Only an admin or owner of this project can change these assignments." | pass |
| `cell5-project-member-readonly-dark.png` | the same in the dark palette | the same | pass |
| `not-taken-organization-agents-tab-light.png` | why the organization frames were not taken | the organization's Agents tab draws the surface placeholder, so no card and no Settings link | recorded |
| `not-taken-agent-permissions-form-light.png` | what the agent's own Permissions page offered | the access picker offers one entry, "Personal: Only me", and it is greyed out | recorded |
| `not-taken-install-settings-access-note-light.png` | what the install's own settings page says about access | "Who can access this extension? Manage who can access this agent from the Agents page." | recorded |

## Not taken

The four organization frames were not taken. An install made at the organization target keeps an
owner-scoped run-data visibility, which the organization, team and project tabs all drop, and no
page in the product widens it for an agent: the install's settings page points at the Agents page,
and the agent's own Permissions page governs a single run and offers nothing wider than the owner.
A team-target install and a project-target install carry the scope token their targets name, which
is how the team and project frames above were reached. No organization-target road produces the
same result today. The round report carries the detail.
