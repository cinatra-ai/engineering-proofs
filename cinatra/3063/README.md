# cinatra — pull request 3063

Full-window captures (1440×900 at device scale 2, light and dark through the app's own theme control) of the email outreach agent's second step for three people created through the app's own sign-up: the run's owner, who is a member of the organisation and not a platform administrator; a member of another organisation, as the control; and a platform administrator. The roles, the run's timeline and the loader's call with the run id are read back on the pull request.

| file | requires | shows | verdict |
|---|---|---|---|
| `step-2-account-scope-member-light.png` | a run owner who is not a platform administrator reaches the second step (Account scope) on the run's own page — no "Not authorized" page; the list picker drawn, with the empty reading where no list exists | the run page with step 2 selected, the picker's empty reading and Continue; the member in the footer | PASS |
| `step-2-account-scope-member-dark.png` | the same in the dark palette | the same reading, dark | PASS |
| `control-other-organisation-light.png` | a member of another organisation does not reach the run: the run page's own refusal, never the administrator page | the run route answering "404 — Page not found" for that member | PASS |
| `step-2-account-scope-platform-admin-light.png` | a platform administrator still reaches the step | the same step 2 for the administrator | PASS |
