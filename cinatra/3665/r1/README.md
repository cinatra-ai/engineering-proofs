# The uploaded skill on the card that offers it, and the scope that does not

Eight counted frames and one recorded frame, taken in a real browser against a
production build of the branch head `23ba7b4195bcfe7cc4bc4b78e0050bd74d29f39b`.
The server was the compiled standalone output, started the way the repository's
end-to-end application workflow starts it: the static assets and the public
folder copied into the standalone tree, the environment file sourced, then the
compiled server started by hand on its own port. No development server ran, and
nothing was rebuilt for these frames.

The instance was fresh. A dedicated database and a dedicated cache held only
this run. The first account registered through the product became the platform
administrator, and the product gave it the Default organization as its active
organization.

## What was supplied, and how

One run tag: `p3607a`.

Two archives, built exactly as the browser walk's own fixture builds them, and
supplied through the Upload Extension screen on the File tab with the scope
picker left where the screen preselects it, at `Workspace: All`:

- `@acme/upload-walk-p3607a-agent`, an agent package carrying the walk's own
  flow document.
- `@acme/upload-walk-p3607a-skill`, a skill package holding one skill file under
  `skills/upload-walk-p3607a-note/`, whose front matter names it
  `upload-walk-p3607a-note`. The catalog renders that name as
  `Upload Walk P3607a Note`.

The screen resolved the kind `Agent` for the first archive and `Skill` for the
second, and it carried the administrator to `/agents` and to the skills listing
after each install.

## The frames

| File | Counted | Palette | What it shows |
|---|---|---|---|
| `cell1-offer-light.png` | yes | light | The card's own assignment page, the Skills pane, the workspace chooser open with the needle typed, and one option row reading `Upload Walk P3607a Note` above `@acme/upload-walk-p3607a-skill`. |
| `cell1-offer-dark.png` | yes | dark | The same reading in dark. |
| `cell2-pick-light.png` | yes | light | The row chosen: the skill now sits on the card as a saved active row with its remove control, and the section counts one of five chosen. |
| `cell3-not-offered-org-light.png` | yes | light | The organization scope named in the heading, its Agents tab reached from that page's own tab strip, and no card for the uploaded agent. |
| `cell3-offered-workspace-light.png` | yes | light | Beside it, in the same run, the workspace Agents tab carrying that card. |
| `cell3-not-offered-org-dark.png` | yes | dark | The same absence in dark. |
| `cell3-offered-workspace-dark.png` | yes | dark | The same presence in dark. |
| `cell4-personal-light.png` | yes | light | The same read answering elsewhere: the personal scope's Agents tab carrying the uploaded card. |
| `recorded-upload-resolved-kind-skill-light.png` | no | light | The Upload Extension screen with the skill archive supplied, its resolved kind line reading `Skill` beside the package name, and the picker at `Workspace: All`. Nothing was installed from this frame; the panel was cancelled. |

## How to read the negative

The install lands at the workspace tier with no owning organization. The scope
reach rule admits such a row at the workspace tier and at a personal scope, and
refuses it at an organization scope. So the organization is the smallest scope
the administrator can reach on a fresh instance that is blind to this install.

An empty tab alone would prove nothing, because the same honest placeholder is
drawn for a read that failed. Two controls stand beside the absence, both taken
in this same run: the organization's Assistants tab renders, which only a scope
whose read completed can do; and the personal scope's Agents tab, drawn by the
same function, carries the uploaded card. What neither control rules out is a
transient failure of the organization's own Agents request.

## Care taken

- The palette of every frame was read off the `<html>` element's class list at
  the moment of the frame, and each reading matched the palette claimed.
- The account name and the e-mail address are painted over in every frame.
- Navigation went through links and tabs: the scope landing, the page's own tab
  strip, the card's Settings link, the organizations listing and the
  organization's own link.

## Anomaly

The organization Agents tab draws the shared placeholder, whose title reads
`This tab is not ready yet`. On this route the tab is fully wired: the page runs
the scope's own eligibility read and falls back to that placeholder when the
read returns no rows. A reader of the frame alone could take the title to mean
the tab is unbuilt. That is a wording matter of the shared shell, not a defect
of this change, and no counted frame depends on it.
