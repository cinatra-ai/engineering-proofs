# cinatra pull request 3709: the empty read draws the tab's own empty reading

Proof rounds for the change that makes the per-scope Assistants and Agents tabs draw
their own empty reading on a read that answered with no rows, instead of the shell's
"This tab is not ready yet" placeholder, which stays for a tab that has no route.

| Round | Head | Result |
|---|---|---|
| r1 | `8bc59ff698131469c173f8b85a0a0200ff333cb3` | 3 counted frames, 0 counted defects, 3 recorded frames; the organization's Assistants tab is never empty because the product unions the built-in assistant into every scope; see `r1/README.md` |
