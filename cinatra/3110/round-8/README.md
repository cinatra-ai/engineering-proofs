# Eighth proof round — pull request 3110 (issue #3033), 2026-09-10

Proof head 2fef3e3c7229f34722e82e1b12b9f1f7e749855e, verified in the worktree with
`git rev-parse HEAD`. A development boot on its own loopback slot, a fresh instance
database cloned from the standard template, the agent runtime container built from
THIS worktree, the first account and the provider sealed through the product's own
screens, the instance namespace set through the product's own name step.

All sixteen frames are the whole window at 1440x960, both palettes through the app's
own theme control, with one reading appended to `dom-readings.jsonl` per shutter and
sha256 / bytes / pixels / mean luminance / bottom-right 300x300 region luminance per
file in `measurements.json`.

The framework's own development indicator is off through the framework's own means:
every reading records `devPortalBox` `0x0`. The app's own topbar wrench ("Open
development tools") exists only because this round ran on a development boot; it is
named here once as that road's artefact and is counted against nothing.

## What was shot

| cell | frames | what the pixels show |
|---|---|---|
| CELL0 | cell0-type-picker-markdown-blog-idea-light, cell0-type-picker-markdown-blog-post-dark, cell0-type-picker-image-blog-image-light, cell0-type-picker-markdown-linkedin-dark, cell0-library-four-typed-light, cell0-library-four-typed-dark | the artifacts area's type picker over a markdown upload offers Blog idea, Post and Post draft among eleven installed types, and over a PNG upload offers Blog image; each of the four uploads was confirmed to its own type and the library then carries the four rows with their type names |
| CELL1 | cell1-blog-idea-artifact-page-light / -dark | the blog-idea display on the artifact's own page, `data-artifact-renderer="blog-idea"`, no picture, no host floor |
| CELL2 | cell2-blog-post-artifact-page-light / -dark | the blog-post display, `data-artifact-renderer="blog-post"`, its own markdown with zero pictures inside it, no host floor |
| CELL3 | cell3-linkedin-post-draft-artifact-page-light / -dark | the LinkedIn post-draft display, `data-artifact-renderer="linkedin-post-draft"`, no host floor |
| CELL4 | cell4-blog-image-display-picture-light / -dark | the blog-image display, `data-artifact-renderer="blog-image"`, exactly one picture drawn from its version-pinned preview route (natural size 1024x576, drawn 1102x620), no host floor |
| CELL13 | cell13-blog-image-library-row-light / -dark | the blog-image library row: the pack's own listRow glyph, carrying the pack's own named floor text "There is no stored version of this picture to show.", not the host's generic glyph |

Two earlier CELL4 files were deleted rather than kept: their shutter fell while the
preview picture was still loading, so they did not contain the state their name
claimed. Their two readings remain in `dom-readings.jsonl` (they record the island
at height 50 with `naturalWidth` 0) and the re-shoot carries new file names.

## What was NOT shot

**CELL5 to CELL8 — NOT SHOT.** These are the review-card cells on the four
displays a real run produces. Three real runs of the blog pipeline were dispatched
through the product's own Run-agent wizard on the sealed session and all three are
attested in the instance database (runtime task id, execution attempt id and an
`immediate` trigger row on each). None of them reached a review card:

1. The first two runs died at the first bridge call because the instance's public
   base URL still named the machine's own default hostname, so the AI provider could
   not reach this instance's public MCP path (HTTP 424). The public base URL was
   changed to this instance's own https origin through the product's own Tunnel
   screen and the app restarted, after which the bridge call answered 200.
2. On the third run the idea step answered, parked at its own "Select blog idea"
   gate — and the five ideas it produced are EMPTY objects. The wizard's gate offers
   "Idea 1 ... Idea 5" with no content, and the runtime records the answer verbatim
   as `{"ideas":[{}, {}, {}, {}, {}]}`. Selecting the first idea and continuing is
   then refused by the pipeline's own passthrough with
   `blog_pipeline_selected_idea: selectedIdeaJson is not a parseable BlogIdea object
   (got "{}")`, and the run fails. The same empty-ideas answer appears on the second
   run as well, so this is deterministic at this head.

   The idea step is an installed agent extension (`@cinatra-ai/blog-idea-generator-agent`
   0.2.0 from the storefront), not host code under this pull request. No blog-idea,
   blog-post, blog-image or LinkedIn post-draft artifact was produced by any run, so
   no review card exists to shoot, and this round's own rule forbids shooting a run
   cell on an uploaded substitute. The four uploads used for CELL0 to CELL4 and
   CELL13 are declared uploads and are never presented as run output.

**CELL9 to CELL12 — not shot, as the round instructs.** They are the recorded
departure filed as cinatra#3330 (the sign-in inside a third-party application frame
fails on a development boot). Nothing was shot and no substitute was used.

## Two instance-road defects fixed during this round, both outside the pull request

* The instance's extension data root was unset, so every install from the storefront
  died with `EACCES: permission denied, mkdir '/data'`. It was pointed at a writable
  directory of this instance and the app restarted; the blog agent packs then
  installed through the product's own marketplace.
* The instance namespace step refuses a namespace containing the reserved substring
  `cinatra`, which the standard bring-up name derives by construction. A clean
  namespace was set through the product's own name step.

## Readbacks (no tokens, no credentials)

* `cinatra.objects` — the four typed uploads:
  `3aabf6f4-…` `@cinatra-ai/blog-idea-artifact:blog-idea`,
  `40be6b2a-…` `@cinatra-ai/blog-post-artifact:post`,
  `370536be-…` `@cinatra-ai/blog-image-artifact:blog-image`,
  `add26b2e-…` `@cinatra-ai/linkedin:post-draft`.
* `cinatra.installed_extension` — the four artifact packs and the blog agent packs
  active on the instance.
* `cinatra.agent_runs` joined to `cinatra.agent_run_triggers` — three runs, each with
  a runtime task id, an execution attempt id and an `immediate` trigger; all three
  ended `failed` for the reasons above. A fourth row was created by a wizard that was
  never dispatched: it carries no runtime task id, so it is a written row and not a
  run, and nothing was shot for it.

The development boot was stopped and the instance database dropped as soon as the
last frame and its reading were written.
