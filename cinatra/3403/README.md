# cinatra#3403 — the setup name step draws the validator reason while editing (issue #3340)

Proof round of 2026-09-11 at head a6b366e014750acb52c84f09f05b3186f5e8bd91 on a development boot whose instance namespace was deliberately left unset, so the name step is open. Every cell is a wizard cell with no agent run. The frames are the namespace field's own bounds (label, note, input, reason) in both palettes; in the two untouched-field frames the input's development prefill is painted over (it carried a machine-derived string that must not be public — the cell's subject is that NO reason is drawn, which the frame still shows). Graded against the three acceptance sentences of #3340 and section I of the setup drawing at design main; structure only.

## CELL3-untouched-quiet-cinatra-field-bounds.png

- **Requires:** CELL3, light, at the field's own bounds: the label, the input and the reason slot — 'An untouched empty field stays quiet' means NO reason is drawn.
- **Shows:** 1400x410 clip over the field-bounds rect (x 370, y 478.89, 700x205.25 CSS), luminance 222.81. Label 'Instance namespace' above; the pre-existing rename note; the white input carrying the prefilled value on the navy hairline; NO red reason line anywhere in the clip; the muted helper line begins below. Paired DOM reading: aria-invalid false, reason null, Continue enabled. Conformance 3 of 3 applicable items.
- **Verdict:** PASS

## CELL3-untouched-quiet-dark-field-bounds.png

- **Requires:** CELL3, dark, at the field's own bounds: no reason drawn on an untouched field.
- **Shows:** 1400x410 clip, luminance 22.34. Label, the rename note (indigo-tinted on dark), the input with the prefilled value on a hairline border, and NO red reason line. Paired DOM: aria-invalid false, reason null. Conformance 3 of 3.
- **Verdict:** PASS

## CELL1-required-reason-focus-kept-cinatra-field-bounds.png

- **Requires:** CELL1, light, at the field's own bounds: the required reason drawn next to the field while the field is still focused, in the existing inline-error styling.
- **Shows:** 1400x466 clip (rect 700x233.25 CSS), luminance 226.30. Empty input with a red destructive border, and immediately below it 'Instance namespace is required.' in brand red at the helper size. Label above, note above the input, muted helper line beginning below the reason. Paired DOM proves focus on the field at the shutter. Conformance 4 of 4.
- **Verdict:** PASS

## CELL1-required-reason-focus-kept-dark-field-bounds.png

- **Requires:** CELL1, dark, at the field's own bounds: the required reason drawn pre-blur beside the focused field.
- **Shows:** 1400x466 clip, luminance 18.59. Red-bordered empty input over a dark ground with 'Instance namespace is required.' in red beneath it; label and note above. Paired DOM proves focus. Conformance 4 of 4.
- **Verdict:** PASS

## CELL2-format-refusal-focus-kept-cinatra-field-bounds.png

- **Requires:** CELL2 format arm, light, at the field's own bounds: the format reason drawn pre-blur beside the focused field.
- **Shows:** 1400x498 clip (rect 700x249.25 CSS), luminance 225.93. 'My Space' in a red-bordered input; the two-line format reason in brand red immediately below, wrapping inside the 672px column. Conformance 4 of 4.
- **Verdict:** PASS

## CELL2-format-refusal-focus-kept-dark-field-bounds.png

- **Requires:** CELL2 format arm, dark, at the field's own bounds.
- **Shows:** 1400x498 clip, luminance 18.57. Red-bordered input carrying 'My Space' with the two-line format reason in red beneath it on the dark ground. Conformance 4 of 4.
- **Verdict:** PASS

## CELL2-reserved-refusal-focus-kept-cinatra-field-bounds.png

- **Requires:** CELL2 reserved arm, light, at the field's own bounds: the reserved reason, naming the word and the fix, drawn pre-blur beside the focused field.
- **Shows:** 1400x530 clip (rect 700x265.25 CSS), luminance 224.85. 'my-cinatra-shop' in a red-bordered input; the three-line reserved reason in brand red below it, the reserved word quoted twice and the approval route drawn as an underlined link. Conformance 5 of 5.
- **Verdict:** PASS

## CELL2-reserved-refusal-focus-kept-dark-field-bounds.png

- **Requires:** CELL2 reserved arm, dark, at the field's own bounds.
- **Shows:** 1400x530 clip, luminance 18.83. Red-bordered input carrying 'my-cinatra-shop' on the dark ground, with the three-line reserved reason in red beneath it and the approval link underlined. Conformance 5 of 5.
- **Verdict:** PASS

## Result

All eight frames PASS; mergeReady true. Two notes from the grader: the whole-step frames of this round stay with the coordinator (they show the development boot's display-name prefill); a pre-existing departure of the namespace field (the red reason line and the muted helper line drawn together) is filed as a follow-up and not counted — it is not this issue's subject.