# Round 2 of 5: the ORGANIZATION scope

These pictures come from a production build of the main branch, started the way
the repository's own end-to-end workflow starts it. No file in the repository
changed to make them.

## The account and the data

Every person, organization, team and project in these pictures is invented for
the proof. The administrator is Ada Example. The two organizations are Aster Org
and Basil Org. The agent is the blog draft writer, handed to the instance as an
upload and installed for Aster Org.

## What the palette reading means

Each picture names its palette. The palette is not guessed from the colours: the
page's own root element is read back after the switch, and the frame is taken
only once the root reports the palette the name claims.

## The package registry

An install of an uploaded agent checks the agent's declared artifact dependencies
against a package registry before it writes anything. Nothing answered at that
address, so the check could not be taken and the first attempt was refused. For
this round the instance ran its own local package registry beside the rest of the
stack, and the three dependencies were published into it at the versions the pack
pins. The check then passed and the install landed for Aster Org.

## What these pictures show, and what is missing

The install landed. The organization holds the agent: the install record and the
agent record both name Aster Org, and both are live.

The organization's own Agents tab still lists nothing. It says "No agents here
yet — No agent is reachable in this scope for you." That sentence is the reason
the round stops here. An install made through the upload page's scope picker with the organization
chosen gives the new agent an owner-only reach, and an owner-only reach never
admits an organization. So the card the
round has to press is never drawn, and every step after it is unreachable.

No control in the product widens that reach. The card's own Settings control,
drawn on the global Agents page, answers a 404 page.

## The cross-organization reading

The round also had to read what happens when a person opens one organization's
agent while the session points at a different organization. That reading needs a
card to press. With no card, it could not be taken at all, in either direction.
It stays open, exactly as it was after the previous attempt.

## The pictures

| File | What it shows |
|---|---|
| `org-s4-install-panel-light.png` | The upload panel, resolved, set to install for Aster Org. |
| `org-s4-install-landed-light.png` | Where the product went after the install: the agents list, with the new agent on it. |
| `org-o1-agents-tab-light.png` | Aster Org, its Agents tab, empty. Light palette. |
| `org-blocker-agents-tab-empty-dark.png` | The same tab in the dark palette. The reading is the same. |
| `org-rec-agents-strip-light.png` | The Agents tab strip of the organization: All Agents and Executions, and no Reviews. |
| `org-blocker-card-settings-404-light.png` | The 404 page the agent card's own Settings control reaches. |
