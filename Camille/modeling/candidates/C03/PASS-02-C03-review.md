# Camille C03 / P02 Zone 3 waist refinement

**Status:** reviewer PASS and planner ACCEPT as a bounded intermediate Zone 3 checkpoint only. This is not final Camille.

## Provenance and approved scope

- Source: `Camille/modeling/candidates/C02/Camille_C02_P02_full-body-athletic-blockout.blend`
- Source SHA-256: `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`
- Candidate: `Camille/modeling/candidates/C03/Camille_C03_P02_zone3-waist-refine.blend`
- Candidate SHA-256: `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`
- Approved visual source: Camille PDF page 2; generated appearance refs, not registered or measured scans.
- Exact zone guide: `C02/P02-zone3-reference-redline.png` SHA-256 `4664F9653FEFE1BFF76DC9A00ABA3A615D95CA344211E63B0770F65D973AB85F`; paired scope note SHA-256 `3508FC350F517CC62ECC645BA78279C4F757F74BF6B84EF4E8EECD7F63FA7531`.

## Isolated edit

Applied a soft symmetric trunk-only field to all five stored shape-key coordinate blocks, retaining their values. The artist-selected field adds up to 2.5% lateral taper and 1.2% anterior depth reduction around a broad waist/lower-abdomen band; actual maximum vertex shifts are 3.661 mm laterally and 1.835 mm anteriorly. The effect fades out before chest and hip transitions and excludes lateral positions outside the torso. These are edit parameters for visual iteration, not measurements inferred from the PDF.

No chest/shoulder, pelvis/glute, head/neck, arm/hand, thigh/calf or foot edits were added. Existing C02 work is retained as the starting state.

## Preservation and measurement status

- Topology: 19,158 vertices / 18,486 polygons.
- Stored shape-key values, object transforms/origin, metric units and Mask settings are preserved.
- No Z coordinate changed; crown, sole and floor Z datums remain unchanged.
- Final anatomical stature remains **UNKNOWN**. No ±0.1 mm height claim is made.
- Circumferences, body-fat value, and clothing-obscured anatomy remain UNKNOWN.

## Review renders

- [Front](P02_front.png) — SHA-256 `1F8D5E4C232AE9EA12275E4C82208F7A42C3BE918717EE8B1AB78965B7D565C8`
- [Left profile](P02_left_profile.png) — SHA-256 `43D27CB56AE48A7802ABA374A80DC65D8660AA6071CBC79970A567B2AA3BFD7D`
- [Rear](P02_rear.png) — SHA-256 `688C7C02C43B4B951B8D8BA9F526EFC04CED6C5B09054CD699716D05C221E024`

Cameras are inherited from C02. Their views show the starter A-pose and are not pixel-registered to the arms-at-sides PDF.

## Review gate

- Reviewer: PASS for the exact candidate hash above; changes remain symmetric and confined to the trunk/waist band, with topology, values, transforms, modifiers and protected Z coordinates preserved.
- Planner: ACCEPT as an intermediate Zone 3 checkpoint only; do not promote as the complete Camille model.
- Corrections: none requested.
- Next zone needs its own bounded redline and exact-hash reviewer/planner loop. Final stature remains UNKNOWN.
