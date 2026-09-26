# Visual proof: the empty read on a scope's Agents and Assistants tabs

These frames come from a production build of the branch head
`8bc59ff698131469c173f8b85a0a0200ff333cb3`. The build was started the way the
repository's end-to-end workflow starts it, against a database created for this
round alone. Every frame was taken in a real browser, in one run, on pages the
browser reached through the product: the Organizations list, then the
organization, then the tab from the page's own tab strip.

The instance is fresh. One account is registered, and that account is the
platform administrator. No agent package and no assistant package is installed
at the organization scope.

Names and the account e-mail address are painted over. The palette of each frame
was read off the root element class of the page itself, not assumed from the
file name.

## The frames

| File | What it shows |
|------|---------------|
| `agents-organization-empty-light.png` | The organization's Agents tab, light palette. The page draws the tab's own empty reading. |
| `agents-organization-empty-dark.png` | The same tab and the same reading, dark palette. |
| `assistants-organization-lists-the-built-in-light.png` | The organization's Assistants tab, light palette. The tab lists the built-in assistant card. |
| `assistants-organization-lists-the-built-in-dark.png` | The same tab, dark palette. |
| `assistants-personal-listed-light.png` | A scope that lists a card: the personal Assistants tab, light palette. |
| `tab-strip-organization-light.png` | The organization page's tab strip, light palette. |

## What the frames prove

On the Agents tab of an organization that reaches no agent, the page says
"No agents here yet" and "No agent is reachable in this scope for you.", and it
offers one action, "Go to Agents". The heading above the strip names the
organization, not the tab. The sentence "This tab is not ready yet" appears
nowhere on the page. The markup was read in the same second as each frame, and
the count of that sentence was zero on every frame here.

The Assistants tab of the same organization lists a card instead of an empty
reading. That is not a fault in the change. The registry reader adds the
built-in assistant to every scope, so an organization always reaches at least
that one assistant and the tab has rows to draw. The frame is kept because it
proves the second half of the same claim: the Assistants tab does not fall back
to the unbuilt-tab sentence either.

The personal Assistants tab lists the same built-in card, which shows that a
scope with rows still draws its list.

## Reading the tab strip

The strip carries Dashboards, Assistants, Agents, Artifacts and Skills in that
order, and the organization page adds Settings after them. The active tab
carries its own state on the element, and the frames show the underline on the
tab the address names.
