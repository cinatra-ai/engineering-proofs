# Proof round — a run's ideas are filed one artifact each, and the review pins exactly those

Head under proof: 08b702fb5a434ab846b3708d3fd911cbe9b9bddb (pull request 3479, issue 3476).

Every frame here is a real page of the running application, reached through the
product's own navigation and signed in through the product's own sign-in page as
the instance administrator. Viewport 1440x1000 at device pixel ratio 2; both
palettes through the application's own theme control. The framework's own
development-server indicator was switched off through the framework's own route
and the page reloaded before each shutter. The account band in the lower left of
the side navigation is painted over in every frame.

## The run

One real agent run of the Blog Idea Generator Agent, dispatched on this boot
through the product's own Run-agent wizard against the sealed provider. It
completed and filed its ideas:

- run 8c10b06a-c07f-465c-9ec1-78c3c6363a7d, runtime task
  e445f5b6-fb76-4fd3-99fe-c177a45d35dc, execution attempt
  356c0484-5ee3-4908-82a4-a15f8eeaacab, trigger immediate, status completed.

The run produced five blog ideas. The product filed each of them as its own
artifact through the fan-out end-node binding (output ids ideas[0] through
ideas[4], every one of them bound and finalized), and filed NO artifact for the
list itself.

## The frames

| file | surface | state | palette |
|---|---|---|---|
| artifacts-list-five-idea-rows-no-json-list-indicator-off-light.png | Artifacts, reached from the side navigation | five Blog Idea rows, one per idea, no JSON list row | light |
| artifacts-list-five-idea-rows-no-json-list-indicator-off-dark.png | Artifacts, reached from the side navigation | the same | dark |
| run-page-review-step-five-pinned-idea-targets-light.png | the run page at its Review step | five pinned idea targets, no JSON list target | light |
| run-page-review-step-five-pinned-idea-targets-dark.png | the run page at its Review step | the same | dark |
| review-page-five-pinned-idea-targets-light.png | Agents, Reviews, Open review | five pinned idea targets, no JSON list target | light |
| review-page-five-pinned-idea-targets-dark.png | Agents, Reviews, Open review | the same | dark |

`measurements.json` carries, per file, the sha256, the byte count, the pixel
size, the mean luminance, the luminance of the required-reading region, the page
URL and breadcrumb read at the shutter, the artifact row count, the pinned
target count and the decision floor read from the page. `dom-readings.jsonl` is
the append-only log of every shutter.

## Readings

- Artifacts list, both palettes: five rows, each one a Blog Idea of media type
  text/plain — When Small Teams Should Not Automate; Automation Metrics That
  Matter for Lean Teams; The Small-Team Automation Audit; How Small Teams Can
  Automate Without Losing Control; Five Automations Every Small Team Should
  Build First. No row of media type application/json, and no row titled after
  the agent. Breadcrumb Artifacts, page URL /artifacts.
- The run page at its Review step, both palettes: the step rail reads Setup,
  Review, What this run made with Review current; the review names exactly the
  five ideas, each marked pinned. Breadcrumb Agents / Blog Idea Generator Agent
  (1).
- The review page, both palettes: the same five pinned targets, breadcrumb
  Agents / 8c10b06a… / Review. The Reviews list above it reads one open gate
  with 5 targets, artifact type @cinatra-ai/blog-idea-artifact:blog-idea, origin
  agent_produced.
- Rows read back read-only (`readbacks.json`): the five artifacts the run
  produced (all of type @cinatra-ai/blog-idea-artifact:blog-idea), the five
  binding rows, the whole object store by type (five blog ideas and thirty agent
  templates, nothing else), zero artifacts of media type application/json, and
  the review gate row with pinnedTargetCount 5 whose five pinned artifact ids
  are exactly the five idea ids.
- The decision floor drawn on both review surfaces on this head reads Comment,
  Reject, Approve. That wording is the subject of a separate issue; it is
  recorded here, not graded.
- The recorder's dry reading is in `recorder-dry-reading.json`: it wrote
  nothing. It read the gate card on the run page as host run_card, state
  pending, with the decision bar present inside the card root, and refused on
  one row — the host declaration is not repeated inside the card root on this
  head.

## Notes on the road

- A development-only control appears in the top bar because this round ran on a
  development boot; it belongs to the road, not to the work under review.
- The first pair of Artifacts frames was taken before the framework's indicator
  route had been reloaded into the page, so the badge was still painted; those
  two files were removed and the cell re-shot under the name carried in the
  table above. Their readings are kept in `dom-readings.jsonl` with a note.
