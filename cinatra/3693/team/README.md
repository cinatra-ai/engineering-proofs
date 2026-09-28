# Round 3 of 5: an agent that belongs to a team

These pictures come from one live instance of the product, started as a
production build and run as the repository's own end-to-end workflow starts it.
No picture is a mock-up and no screen is drawn by hand. The account is invented:
Ada Example, the first person to register, who is the platform administrator and
an administrator of the team. Every step below was taken by pressing something
the product drew on the page, never by typing an address, unless the text says
otherwise.

The scope is a team named Aster Team, inside an organization named Aster Org.
The agent is the Blog Draft Writer Agent. Its one input is a single line of
text, the idea for a post. The line used throughout is: "Why every team needs
one shared notebook".

Each picture is named for its step and for its palette. The palette is not
guessed: the page root was read back before every frame, and it answers either
"cinatra" for the light palette or "dark" for the dark one. Where both palettes
exist, they carry the same words and the same controls, and differ in colour
only.

## How the agent came to belong to the team

An earlier record of this package was left behind by an earlier proof run, and
that record refused every new install. It was removed through the product's own
extension settings page, with the Force-delete control and a typed reason, and
the product then reported that it had cleaned up the dangling references. The
agent was installed again straight afterwards, through the upload page, with the
page's own scope picker set to the team. The picker offers the team by name, and
the record the install wrote names the team in all three of its visibility
fields. Both halves of this are visible in the pictures: the settings page
before and after the removal, and the upload panel with the team chosen.

The instance ran a package registry of its own, on the same machine, so the
install could check the three packages this agent depends on.

## The cross-organization reading

One reading was taken on purpose with the wrong organization active in the
session: Basil Org, which does not contain this team. Two things happened, and
both are in the pictures.

First, the good news: the team's Agents tab still lists the agent, pressing Run
still opens the launcher, and the run the product created is filed against the
team's own organization rather than the one the session happened to hold. That
is the behaviour the scope model promises, and it holds.

Second, the team's own front page refuses. Pressing the Dashboards tab, or the
team's own crumb in the trail, lands on a page that reads "Not authorized. This
area is limited to platform admins", although the signed-in person is exactly
that. On the same screens the team's name does not resolve either: the trail
shows a shortened raw identifier and the heading reads the bare word "Team"
instead of "Aster Team". Both are recorded as faults of this round.

## What the run reached, and where it stopped

The run was started from the card, given its one line of text, and taken through
its Schedule and Permissions views. It then paused at its context gate, which
drew in place on the run's own page rather than as a separate document, and
offered the person's own saved idea. That selection was made and accepted, and
the product recorded it.

The run stopped there. The model account behind this instance has no credit
left, and the model service answered that plainly, so no draft was ever written.
The pictures named "model blocked" show the stopped card. The later steps that
needed a written draft could not be reached, and the report says so rather than
claiming them.

The run's successor, started from the stopped card, lands under the team's own
address and carries the same anchor as its parent. The run list under the team's
Executions tab holds all of the runs. The notices on the global notifications
page point at each run's own page under the team, never at a separate review
document.
