# Round 4 of 5: the project scope

These pictures come from one instance of the product, built for production from
the current main line and started the way the repository's own end-to-end test
workflow starts it. No development server took part. The account is invented:
Ada Example, ada@example.test, the first person to register, so the platform
promoted the account to full access. The palette of every frame was read back
from the page root before the shutter, so a light frame is light and a dark frame
is dark by the page's own word for it.

## Why the round's project is a team-owned project made for it

The round needs a project whose Agents tab can list an uploaded agent. The upload
page's scope picker offers a project only when the signed-in person owns it, or
when a team the person belongs to owns it. The organization-owned project that
three earlier rounds worked beside was therefore never offered, and the picker
showed four choices with no project among them. So this round first created a
project through the product's own New project form, set its ownership level to a
team and picked the team, and only then opened the upload page. The picker then
offered the project as its first choice. This is a property of the picker, not a
fault: an organization-owned project has no install authority the picker can
prove for the person in front of it.

## The reading taken with another organization active

The round also took one reading with a second organization active in the session
while the project belonged to the first. The project's Agents tab still listed
the card, the project's own front page opened normally, the heading and the trail
both read the project's name rather than an identifier, and pressing Run opened
the launcher with no error. The run it made was filed against the organization
that owns the project, not against the one the session held. So the run follows
the scope. Nothing on the project surface resolved itself against the session
instead of against the scope, which is the fault the team round found on its own
surface.

## Which road installed the agent

One road was enough: the archive was uploaded straight over the package's live
team install, with the picker set to the project, and the product accepted it and
re-pointed the access policy at the project.

The instance ran a package registry of its own on the same machine, so the
install could check the agent's declared dependencies.

## The frames

| Frame | What it shows |
|---|---|
| `project-seed-form-light.png` | The New project form, filled, with team ownership chosen and the team picked. |
| `project-seed-created-light.png` | The project the form made, on its own front page. |
| `project-s4-install-panel-light.png` | The upload panel, the agent read from the archive, the scope picker set to the project. |
| `project-s4-install-t3-light.png` | The upload page three seconds after the install was pressed. |
| `project-s4-install-landed-light.png` | Where the install landed: the agents index, the card listed. |
| `project-p1-light.png` / `-dark.png` | The project's Agents tab and the agent's card, both palettes. |
| `project-p2-light.png` / `-dark.png` | The run, on its own page under the project, both palettes. |
| `project-p3-light.png` / `-dark.png` | The run's Schedule view, both palettes. |
| `project-p4-light.png` / `-dark.png` | The run's Permissions view, reading the project by name, both palettes. |
| `project-p5-light.png` / `-dark.png` | The context gate, drawn in place on the run's own page, both palettes. |
| `project-p5-selected-light.png` | The same gate with the offered artifact chosen. |
| `project-p6-light.png` / `-dark.png` | The gate after the decision was accepted. |
| `project-p6-settled-light.png` / `-dark.png` | The run read again after the decision, both palettes. |
| `project-p7-model-blocked-light.png` / `-dark.png` | The stopped card. The model service refused the call. |
| `project-p8-light.png` / `-dark.png` | The same card, read as the completion card. |
| `project-p8-successor-light.png` | The next run, started from the stopped card, under the project, at its first step. |
| `project-p9-light.png` / `-dark.png` | The project's Executions list, both palettes. |
| `project-p10-light.png` | The notifications page. Every run notice points at a run's own page under the project. |
| `project-p0-tab-other-org-active-light.png` | The project's Agents tab with another organization active. |
| `project-p0-landing-other-org-active-light.png` | The project's own front page, reached from that tab, with another organization active. |
| `project-p0-run-other-org-active-light.png` | The launcher, opened with another organization active. No error. |
| `project-rec-agents-strip-light.png` | The tab strip: All Agents and Executions, no Reviews. |
| `project-rec-team-tab-after-project-install-light.png` | The team's Agents tab after the project install: empty, correctly. |
| `project-rec-org-tab-light.png` | The organization's Agents tab: empty, correctly. |
| `project-rec-what-this-run-made-light.png` | What the run made and what it read, drawn in place on the run's page. |
| `project-rec-personal-tab-light.png` | The personal Agents tab, which lists the card as well. |

## What the round could not show

The draft itself was never written. The model service behind the instance answers
that the account has no credits remaining, so the finished card, a review of a
written draft and a publish step were all out of reach. Those frames are marked
as blocked rather than failed: the product reached the model and the model
refused to answer.
