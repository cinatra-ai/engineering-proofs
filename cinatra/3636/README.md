# Proof round p3636: a member's More details modal on a real page

Head commit: `3835118d3eb7c5c3b1dec6d627d7d35616502d99`. Every frame is bound to it. No file of the
product tree changed in this round.

## What was seeded, and how

Everything below was done through the product in a real browser, on a fresh database.

1. The first account registered on the setup screen. It became the platform administrator
   (role `admin`) and the owner of the Default organization.
2. As the administrator: Configuration, Access control, the card "Self-registration", the control
   "Allow new sign-ups" turned on.
3. In a second browser context with no session: the sign-up screen, a second account registered.
   It received the role `user`. At its first sign-in it joined the Default organization as
   `member`. Its sidebar carries no Analytics entry and no Configuration entry, so it is not an
   administrator.
4. As the administrator: "Allow new sign-ups" turned off again.
5. The card: the boot holds 94 installed packages and none of them is anchored to an
   organization. The organization Agents tab therefore lists nothing and draws its empty state.
   The round used the fallback the pull request body names: the Workspace Agents tab, which lists
   the 30 platform-level agent packages that carry the default audience. The card pressed is
   "Agent Code Reviewer".

Account names and e-mail addresses are painted over with a solid block before every capture.

## How each page was reached

Sidebar, Workspace, the Agents tab. Then the card's own More details control. The palette was set
through the stored theme value and the page reloaded; the document class was read back on every
frame (`cinatra` for light, `dark` for dark).

## The frames

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `member-more-details-modal-light.png` | A member who is not an administrator presses More details on an agent card of a scope page, and the modal draws the package's name, its vendor and its detail body. Light palette. | The modal over the Workspace Agents tab. Emblem tile, the name "Agent Code Reviewer", the byline "Agent by Cinatra AI", the licence line "Open source", the tab row with Details selected, the detail body with its heading, paragraph and capability list, and the facts column with version, last updated, compatibility and installation count. | PASS |
| `member-more-details-modal-dark.png` | The same modal, dark palette. | The same modal and the same content on the dark surface. Document class `dark`. | PASS |
| `member-agents-card-light.png` | The agent card itself with its More details action, as the member. | The three-panel card: coloured tile panel with the name and the "Agent by Cinatra" byline, the description panel, and the action panel with Run, then Settings and More details side by side. | PASS, with one recorded mismatch: the card byline names the vendor "Cinatra" while the modal names it "Cinatra AI". |
| `member-agents-page-light.png` | The page the card sits on, as the member. | The Workspace Agents tab with its tab row and its list of agent cards. The member sidebar carries no Analytics and no Configuration. | PASS |
| `admin-more-details-modal-light.png` | The control: the same modal as the administrator. | The same modal with the same content. Only the page behind it differs: the administrator sidebar carries Analytics, and the top bar carries a settings control. | PASS |

## Recorded, not counted

- The modal carries a share row at its foot with five outbound share links. The drawing for this
  modal says it carries no footer of its own. This is a deviation from the drawing; it is not a
  defect of this pull request, and nothing in the change touches it.
- The modal shows no dependency list and no code block. Both are data of the package shown, which
  declares neither.
- The instance ran without a marketplace attachment, on purpose. The effect is recorded in the
  round's report.
