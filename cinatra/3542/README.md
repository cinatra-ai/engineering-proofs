# Proof round 2 for pull request 3542: the extension settings page

Head commit: `9e1de5918278326c25ef2beacade6d8f6d4b8724`. Every frame in this folder is bound to this head.

## How the pages were reached

- A development installation of this head, on a fresh database, signed in as a throwaway admin account.
- Clicks only: Configuration, then the Extensions card's "Installed" link, then the card's "Settings" button.
- The agent is "Agent Code Reviewer" (`@cinatra-ai/code-reviewer-agent`). The connector is "Apify" (`@cinatra-ai/apify-connector`).
- The Register frame follows the "Register for marketplace" link on the agent's settings page.
- The palette comes from the product's own stored theme setting. The page root carried the class `cinatra` (light) or `dark` (dark) on every frame.
- The installation is not a registered marketplace vendor. It is not attached to the live marketplace: the Registries tab reads "Not attached". No registry answers on the installation.
- A solid grey block covers the signed-in account (name and e-mail address) in the sidebar before every capture. No other name or address shows in the frames.
- The framework's development indicator was switched off through its own route before the first capture. The wrench in the top bar exists only on a development installation.

## Files

| File | Requires | Shows | Verdict |
|---|---|---|---|
| `settings-header-byline-agent-light-r2.png` | Counted. The header of an installed agent: the kind glyph, then "Agent by Cinatra" from declared vendor data, kind and vendor in ink, "by" muted, nothing at the top right. | The robot glyph in the agent's accent colour, then "Agent by Cinatra". "Agent" and "Cinatra" are in ink, "by" is muted. Nothing sits to the right of the name. | Pass |
| `settings-header-byline-agent-dark-r2.png` | Counted. The same header in the dark palette. | The same reading holds. | Pass |
| `marketplace-group-agent-register-gate-light-r2.png` | Counted. The Marketplace group of an installed agent on an instance that is not a registered vendor: a muted red "Publish on marketplace" with the store glyph, beside an outline "Register for marketplace" link with the external-link glyph. No "Published on the marketplace." line. | Exactly that pair on one row. The publish button is disabled and faded. There is no published line and no other text. | Pass |
| `marketplace-group-agent-register-gate-dark-r2.png` | Counted. The same group in the dark palette. | The same reading holds. The faded red label is very faint on the dark ground (recorded, see below). | Pass |
| `marketplace-group-connector-register-gate-light-r2.png` | Recorded. The same group on an installed connector. | The same muted publish button beside "Register for marketplace". No published line. | Recorded, matches |
| `marketplace-group-connector-register-gate-dark-r2.png` | Recorded. The same group on the connector, dark palette. | The same reading holds. | Recorded, matches |
| `register-link-destination-light-r2.png` | Recorded. "Register for marketplace" opens Environment on its Registries tab. | The Environment page with the Registries tab selected: the "Marketplace connection" card ("Not attached") and the "Become a vendor" card with "Apply for vendor status". | Recorded, matches |
| `settings-page-agent-light-r2.png` | Context. The whole settings page of the agent. | Header, Permissions, Execution, Marketplace, Maintenance, Danger zone. | Context |
| `settings-page-agent-dark-r2.png` | Context. The same page in the dark palette. | The same groups. | Context |

## Not reached on a development installation

- The registered-vendor state (the muted action beside "Marketplace publishing isn't available for this extension yet.") needs a vendor registration on the live marketplace. The rendered test "a registered vendor viewing a kind that can't be published yet: muted action beside the VISIBLE reason" in `src/app/configuration/extensions/settings/__tests__/extension-settings-byline-and-publish-gate.test.tsx` pins that reason as visible text.
- The live publish action needs the same vendor registration and an agent stored as private with a known version.

## Recorded, not counted

- In the dark palette, the faded red publish label is very faint. The product fades the button to 0.5; the drawing uses 0.45. The rule says "muted", so this is not counted.
- The disabled button's pointer is the plain arrow; the drawing uses the "not allowed" pointer. A still picture cannot show a pointer.
- The drawing prints the link's destination path as a muted note beside the link. The page does not print it. This reads as a note of the drawing, not a part of the page.
- The Execution group between Permissions and Marketplace is not drawn in section V. It is already filed and is outside this pull request.
- The breadcrumb shows "@Cinatra Ai", the raw scope with capital letters. It is outside section V and outside this pull request.
- On the Registries tab, the tab strip draws a doubled rule to the right of the tabs. This pull request does not touch it.
