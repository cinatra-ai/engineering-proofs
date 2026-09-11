# cinatra#3409 — the extensions marketplace conformance batch (#2735, #2736, #2737)

Third proof round, 2026-09-12, at head 89e1329dacb2ce53ebe7e6bd05a6cf11e6088b51 on a sealed development boot with the runtime container up (no agent run is part of these cells: the marketplace, the detail modal and the install panel are [no run] surfaces). Twelve frames: the detail modal's overlay (#2735), the modal's Details, Reviews and Changelog tabs and the retired legacy route (#2736), the listing cards with the in-card install panel closed and open on a long-title and a short-title card (#2737); light and dark. The sidebar's bottom band is painted over in every frame (it carried the lane's account label). Graded against the checklists of the three issues and sections I and II of the extensions drawing plus the components drawing's dialog rule at design main; structure only.

## cell1-detail-modal-overlay-light.png

- **Requires:** C12 (#2735, and specs/app-components.html: 'Overlay top: 4rem so it doesn't cover the navbar' / 'the overlay dims everything below the 4rem navbar'): with a modal open the overlay dims the sidebar and the content below the 4rem navbar and the navbar itself stays undimmed; structure: the overlay's top edge coincides with the navbar's bottom edge, the dialog sits on --paper above it.
- **Shows:** overlayComputedTop 64px = 4rem, background oklab(0 0 0 / 0.5), position fixed, z-index 145, overlayBox {0,64,1440,836}, navbarBox {256,0,1184,64}, navbarBottomVsOverlayTop 0; sidebarBackdropDimmed true, contentBackdropDimmed true, navbarDimmed false. My own re-measurement of the PNG against the no-modal frame of the same page: sidebar below 4rem 232.48 -> 115.76 (an exact halving, the 0.5-alpha layer), content 218.62 -> 108.76, navbar 237.88 -> 237.88 (delta 0.00), the sidebar's own 0..64 brand band 229.76 -> 229.76 (undimmed, consistent with a full-width overlay whose top is 4rem). A side-by-side crop confirms the dimming visually; no reading contradicts its frame. Dialog on the paper surfa
- **Verdict:** PASS — 3 of 3 applicable items (conformance 3/3, 100%). Structure right: one overlay region, top edge exactly at the navbar's foot, nothing docked in another region's place.

## cell1-detail-modal-overlay-dark.png

- **Requires:** C12 in the dark palette: same overlay geometry and the same three backdrop states.
- **Shows:** Identical geometry: overlay top 64px/4rem, overlayBox {0,64,1440,836}, navbarBottomVsOverlayTop 0, sidebarBackdropDimmed true, contentBackdropDimmed true, navbarDimmed false. My re-measurement against the no-modal dark frame: sidebar below 4rem 17.42 -> 8.70 (halved), content 40.50 -> 19.74, navbar 9.52 -> 9.52 (delta 0.00), brand band 31.84 -> 31.84. Luminances sit inside the dark band; dialog paper reads 18.63.
- **Verdict:** PASS — 3 of 3 applicable items (3/3, 100%).

## cell2-detail-modal-details-tab-light.png

- **Requires:** C11 and C13 plus the section II caption sentences: More details opens the modal; its body is the listing detail lifted whole (app-logo tile, title, {Type} by {Vendor}, price, the Details / Reviews / Changelog tabs, README beside its specs column with version, last-updated, Compatible up to, installations, and the share row); stripped of the site header/footer, the storefront's Install now, the More Extensions tab, pagination and the Related extensions rail; no footer and no install/update/restore control of any kind; the header carries just a close mark; title equals the manifest displayName; 
- **Shows:** dialogOpen true, dialogBox {360,80,720,804}; tabs ['Details','Reviews (0)','Changelog'], tabCount 3, selectedTab Details, Details panel 2443 chars over 25 lines; footerCount 0; installControlsInDialog []; closeControlsInDialogTotal 1 with closeInHeaderBand true, aria 'Close'; dialogOwnConformanceId 'extension-detail-modal'; title 'Chat Assistant Core Skill' equal to the manifest displayName read back from the pinned pack. Visible: logo tile, italic title, 'Skill by Cinatra AI' byline with the kind glyph, the price 'Open source' on the right, the tab row with the drawing's own paired-line rule beside it (section I markup: a 5px element with 1px top and bottom borders in an auto/1fr grid — so 
- **Verdict:** PASS — 14 of 14 applicable items (14/14, 100%). Every visible element traces to a drawing sentence; no unspecified element inside the dialog.

## cell2-detail-modal-details-tab-dark.png

- **Requires:** C11 and C13 in the dark palette.
- **Shows:** Identical DOM readings to the light frame (3 tabs, footerCount 0, installControlsInDialog [], one close control in the header band, conformance id present, title equal to displayName, panel 2443 chars / 25 lines). Dialog paper and body luminances inside the dark band; the dimmed grid behind it reads as in CELL1 dark.
- **Verdict:** PASS — 14 of 14 (100%).

## cell2-detail-modal-reviews-tab-light.png

- **Requires:** C13's clause 'Details, Reviews and Changelog tabs render their content', and the section II caption: the reviews list beside its rating summary (the average, the star-by-star breakdown and per-level counts, the submission form dropped in-app), then the share row; still no footer and no install control.
- **Shows:** selectedTab 'Reviews (0)'; panel {387,304,666,205}, 96 chars over 10 lines, first lines ['0 reviews for Chat Assistant Core Skill','No reviews yet.','Rating summary','0.0','0 reviews','0','0','0','0','0']. The frame shows the empty-state list on the left and the rating summary on the right — average 0.0, five stars, '0 reviews', a five-row star-by-star breakdown with per-level counts — then a rule and the share row (five share marks). No submission form, footerCount 0, installControlsInDialog [], one close control in the header.
- **Verdict:** PASS — 7 of 7 applicable items (7/7, 100%); the panel renders its content, as the clause requires.

## cell2-detail-modal-changelog-tab-light.png

- **Requires:** C13's tab clause plus the section II sentence: the Changelog tab renders the root CHANGELOG as per-version release notes, or a 'No changelog available' message when the extension ships no CHANGELOG; the drawing's own no-CHANGELOG example is an icon above that message.
- **Shows:** selectedTab 'Changelog'; panel {387,304,666,158}, 22 chars, one line, ['No changelog available']. The frame shows the file-with-cross mark above the bold 'No changelog available', then the rule and the share row. footerCount 0, installControlsInDialog [], one close control in the header band.
- **Verdict:** PASS — 5 of 5 applicable items (5/5, 100%); the wording matches the drawing exactly.

## cell2-legacy-route-grid-light.png

- **Requires:** C13's last clause: the legacy detail route redirects to the plain grid without auto-opening the modal; and C2's resting card layout on the grid it lands on (price on its own centred line above, install control and More details side by side beneath it, details on the right; no vendor-name checkmark on the byline).
- **Shows:** addressBar read after navigating /configuration/marketplace/cinatra-ai/chat-assistant-core-skill: 'the boot's address/configuration/marketplace'; dialogOpen false, anyDialog false, gridCardCount 83. The frame shows the plain grid with nothing open, three columns at this breakpoint (the drawing contracts three or four), each card carrying the centred price line then Install now with More details to its right, and no checkmark beside any vendor name. The redirect itself is carried by the DOM address reading, not by the pixels (a headless frame paints no address bar) — recorded as such.
- **Verdict:** PASS — 6 of 6 applicable items (6/6, 100%).

## cell2-legacy-route-grid-dark.png

- **Requires:** The same legacy-route clause and card layout in the dark palette.
- **Shows:** Same readings (addressBar back on /configuration/marketplace, dialogOpen false, anyDialog false, 83 cards); palette luminances inside the dark band, card faces and action rows as in the light frame.
- **Verdict:** PASS — 6 of 6 (100%).

## cell3-cards-panel-closed-light.png

- **Requires:** C10 and C14: the idle card face at the fixed block size (299px) that the open panel must match, on a long-title card and a short-title card; C2's one-line action row.
- **Shows:** cardHeights [299,299]; 'Google Appointment Schedules' titleLength 28 box {661,231,373,299}, 'Chart' titleLength 5 box {1051,231,373,299}, panelOpen false and the install control live on both. My own column profile of the PNG puts the card top at 231 and the foot at 530 CSS (299px) with the next grid row starting at 547. Action row is one line with the price centred above it.
- **Verdict:** PASS — 4 of 4 applicable items (4/4, 100%); this frame is the height baseline the open frame is held to.

## cell3-cards-panel-closed-dark.png

- **Requires:** The same idle baseline in the dark palette.
- **Shows:** cardHeights [299,299] with identical boxes; my pixel bounds for both card columns are byte-identical to the light frame's and to the open dark frame's.
- **Verdict:** PASS — 4 of 4 (100%).

## cell3-both-cards-panel-open-light.png

- **Requires:** C9, C10 and C14: Install now swaps the card's body in place with no popup; the header band (icon, name, byline) is kept and only the body is replaced by the install panel — the access-scope picker preselected to Workspace: All and Cancel / Install now actions; a close mark in the header's corner; the eyebrow adjacent to the picker as section I.1 draws it; the panel at the same block size as the idle card (299px) so the grid row never jumps; errors are a toast, never inline.
- **Shows:** Both a long-title card (28 chars) and a short-title card (5 chars) open at once. cardHeights [299,299]; box h 299 on both, identical to the closed frame — my own column profile again reads top 231, foot 530, next row at 547, unchanged between the two states. No dialog element appears (the swap is in place). Header band keeps icon, name and byline; card text becomes ['<name>','<kind> by Cinatra AI','INSTALL FOR','Workspace:','All','Cancel','Install now']. eyebrowText 'Install for' (uppercased by the drawing's own mono style), eyebrowBox {676,379,343,12} sits 10px above pickerBox {676,401,343,32} sharing its left edge and width; pickerText 'Workspace:All' preselected; Cancel outline and Instal
- **Verdict:** PASS — 9 of 9 applicable items measured (9/9, 100%); the failed-install toast clause was not exercised this round and is recorded as a gap, not a miss. Structure right: the panel is inside the card frame, never a dialog, and no region is docked in another's place.

## cell3-both-cards-panel-open-dark.png

- **Requires:** C9, C10 and C14 in the dark palette.
- **Shows:** Identical readings: both panels open, cardHeights [299,299], eyebrow 'Install for' 10px above the picker in the same column, picker preselected 'Workspace:All', close control in the header corner with aria 'Close install panel', Cancel / Install now at the foot, toastCount 0, no dialog. My pixel bounds match the dark closed frame exactly.
- **Verdict:** PASS — 9 of 9 (100%).

## Result

All twelve frames PASS; mergeReady true; no counted defect. Follow-ups recorded by the grader, none counted: the 'Compatibility unknown' third state of the card foot (a shipped state the drawing has not caught up with), platform-owned packs carrying an enabled Install now (a deliberate shipped semantics), the long title re-wrapping to two lines when the panel opens, and one clause not exercised (a failed install toasts, never inline).