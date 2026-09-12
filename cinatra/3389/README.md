# cinatra#3389 — the connector Sharing tab: the recommending connector's line and the stored grant (#3374, #3408)

Proof round of 2026-09-12 at head ddb72690a100b92ac55a15800da1d3f3d61f0540 on a sealed development boot: a new server registered through the MCP Servers connector's own Setup form (CELL3, the fresh panel: the recommendation line stated word for word, the picker on the stored grant), a real save of the recommended scope on that connection (CELL4: the panel re-reads the saved scope, no recommendation line), and the locked treatment read on the conformance harness (CELL6, a recorded gap: no fleet connector that declares a ceiling holds a connection). Light and dark. The sidebar's bottom band is painted over in every frame. Graded against the issues' sentences and section II of the connectors drawing at design main; structure only.

## cell3-recommendation-light.png

- **Requires:** §II Sharing tab, checklist items applicable to a recommending connector's panel: (1) a list of panels, one per connection you own here; (2) each a connection row carrying its name and mono line and nothing else — no status badge, no per-row action; (3) beneath each row the shared permissions card on the --surface ground; (4) Access — the scope picker, ordered narrow to broad, drawn with the --line-strong navy hairline on a --surface-strong ground; (5) helper 'Choose who can use this connection.'; (6) Ownership — a 'Search by name or email…' field; (7) helper "Owners can change this connection'
- **Shows:** Two full panels and part of a third. The round's own connection external-mcp-09372018-8d74-4717-a226-399e706239fb renders as a row card (bold name, mono 'externalMcp', no badge, no action) with the permissions card beneath on measured ground rgb(247,247,243) = --surface. Access picker white (255,255,255) reading 'Personal: Only me' — the STORED grant — then, under it, a lock glyph and the line verbatim: 'This connector recommends sharing with the whole workspace — nothing is shared until you save. Currently: only you.', then 'Choose who can use this connection.'. Ownership: 'Search by name or email…' field with a measured rgb(21,33,58) = --line-strong navy hairline, helper verbatim, one owne
- **Verdict:** PASS — 11/12 (92%). Behaviour (a) passes: the line is stated and the picker sits on the stored grant. The one miss is (b) and pre-existing: item 4's picker hairline renders grey rgb(215,217,216) instead of the drawn --line-strong navy — the shared AccessCombobox trigger's own `border-line` class (src/components/access-combobox.tsx:788), not introduced by this branch; the Ownership field beside it 

## cell3-recommendation-dark.png

- **Requires:** The same twelve items, structure only: the ratified specs draw no dark palette at all (app.html defines one light canonical palette), so no dark colour band is gradeable and none was invented.
- **Shows:** Structurally identical to the light frame at the pixel level of layout: same row card, same permissions card, same picker reading 'Personal: Only me', the same lock-led line verbatim, the same two helper lines, the same single owner row with the lock in the remove slot, the same one right-aligned 'Save changes'. Frame luminance 15.34, region 20.60. The only palette-level difference is that the primary 'Save changes' inverts to a light pill — the app's dark mapping, undrawn.
- **Verdict:** PASS — 11/12 (92%), the same single pre-existing picker-hairline miss carried over from the light frame. Dark colour values ungraded, by the drawing's own silence rather than by concession.

## cell4-saved-scope-light.png

- **Requires:** §II items 1-9 above, plus: the grant is written when Save changes is pressed and not before; once the stored grant is the owner's own explicit choice the recommendation line no longer stands (the drawn sentence presupposes 'Currently: only you.').
- **Shows:** The round's own panel now reads 'Workspace: All' with NO line between the picker and 'Choose who can use this connection.' — the helper sits directly under the trigger, exactly as the un-recommended panel beside it. Row card, permissions card ground, Ownership field and helper, the locked owner row and the single right-aligned --blue 'Save changes' are unchanged. The database read-back makes the save real, not cosmetic: the policy moved from the connect seed {seededDefault:true, …["owner"]} to {allowRunSharing:false, runData/List/ExecuteVisibility:["workspace"]} at 01:43:05.673991+00 with the seededDefault marker stripped. No audit row was written by the save — correct, and the round's own s
- **Verdict:** PASS — 10/11 (91%). Behaviour (a) passes on a real save on the round's own connection, with the stored policy read back. The single miss is the same pre-existing shared-picker hairline.

## cell4-saved-scope-dark.png

- **Requires:** The same eleven items, structure only (no dark palette is drawn).
- **Shows:** Structurally identical to the light CELL4 frame: 'Workspace: All' on the trigger, no line, helper directly beneath, the rest of the card unchanged. Frame luminance 15.21, region 20.26.
- **Verdict:** PASS — 10/11 (91%), same single pre-existing miss; dark colour values ungraded by the drawing's silence.

## cell6-locked-harness-light.png

- **Requires:** §II 'access locked by the connector': (1) the picker renders every option above the ceiling locked, each carrying the sentence as its reason; (2) the same sentence sits under the picker WITH A LOCK; (3) the helper 'Choose who can use this connection.' beneath it; (4) the trigger shows a value within the ceiling; (5) the picker chrome as drawn; (6) the roll-up is the Connections status card with no Check and no All connections link; (7) the row carries name and mono line and nothing else.
- **Shows:** The locked treatment, rendered by the product component but on the repository's own conformance harness route (/design-fixtures/conformance) with fixture data ('quimbly-vetch-0417' / 'brindlewick'), because no pinned-fleet connector that declares a ceiling holds a connection on this boot. Trigger 'Workspace: Admins only'; beneath it a lock glyph and 'Locked by this connector: access is limited to workspace admins (only:"admin").'; beneath that 'Choose who can use this connection.' — the drawn three-line stack exactly. data-variant="locked". The roll-up card above reads 'Connections status' with a single green '1 Connected' badge, no Check button and no All connections link. Lower in the same
- **Verdict:** GAP, not a pass — 5 of 6 gradeable items hold (83%), item 1 is unproven (the option list was never opened, so the locked/disabled options and their per-option reason were not seen), and item 5 carries the same pre-existing picker-hairline miss. The cell cannot count as proof of the locked surface at all: a fixture route is a stand-in, never the product surface. The rail sanctioned recording it as 

## cell6-locked-harness-dark.png

- **Requires:** The same seven items, structure only.
- **Shows:** Structurally identical to the light harness frame: same locked trigger value, same lock-led sentence, same helper, same roll-up with no Check and no All connections link. Frame luminance 16.52, region 20.50. The '1 Connected' badge renders a bright green rather than the muted --green of the light frame — a dark-theme mapping the ratified specs do not draw.
- **Verdict:** GAP, not a pass — same 5/6 (83%) as the light frame, same unproven option-list item, same fixture-route limitation.

## Result

CELL3 and CELL4 PASS in both palettes; CELL6 is a recorded gap (harness evidence only); mergeReady true. Follow-ups recorded by the grader, none counted: the picker's grey hairline (pre-existing, the shared combobox's soft token), the recommendation line rendering with a lock glyph (a drawing ambiguity), the tab strip carrying no Connections tab for a many-connection connector (to verify against the drawing).