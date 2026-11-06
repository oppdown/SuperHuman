# Camille C02 / P02 full-body silhouette blockout

**Status:** Reviewer PASS and planner ACCEPT as a mechanics-verified intermediate broad-silhouette candidate. This is not final Camille likeness, character, height, or rig acceptance.

## Provenance and references

- Source candidate: `Camille/modeling/candidates/C01/Camille_C01_P01_stature-normalized.blend`
- Source SHA-256: `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`
- Candidate: `Camille/modeling/candidates/C02/Camille_C02_P02_full-body-athletic-blockout.blend`
- Candidate SHA-256: `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`
- Appearance authority: `Camille/specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf`, SHA-256 `264973DF0712F947917AA6F8EA9E6726D7CB13914B5260FF0350935AC0161A99`.
- Scope map: `Camille/modeling/candidates/C01/P02-fullbody-reference-map.png`, SHA-256 `70EDA4BD2C6CCC45E94FC3E93D86474FDC4B9C9D13809377D7D92B45DE74EA7B`.
- PDF views are generated appearance references, not calibrated scans. P01 is the editable starter-derived source only; no earlier Camille geometry was used.

## Applied changes

A modest symmetric silhouette field was applied to all five saved shape-key coordinate blocks while retaining stored values: broader chest/shoulder and pelvis silhouettes, maximum 8.5% lateral waist reduction around the waist center, a small posterior glute fullness cue, lightly adjusted thigh/calf widths, and a provisional 18 mm inward horizontal translation per foot at the contact area, fading toward the ankle. The 18 mm stance adjustment is an artist-selected iteration value, not a PDF measurement.

The head/face/ears and arm/hand geometry remain starter-derived. Hair, unitard, materials and rig are not present. The PDF arms-at-sides vs P01 A-pose mismatch remains; no arm-span or exact axilla inference is claimed.

## Preservation and measurement status

- Topology remains 19,158 vertices / 18,486 polygons.
- All five saved shape-key values are unchanged.
- Object transforms, metric units and `Hide helpers` Mask settings are unchanged.
- No vertex Z coordinate changed. The current provisional crown, floor and sole Z datums remain in place. Foot shape was preserved while the feet moved horizontally.
- Reviewer’s separate-process Blender 5.2.1 audit found symmetric XY displacements across 18,804 mirror pairs; evaluated mesh remains 13,380 vertices.
- Final stature remains **UNKNOWN**; this pass makes no ±0.1 mm stature claim. Other unmeasured anatomy remains UNKNOWN or provisional.

## Inherited source shading note

The dark/flat posterior thigh-glute fold patch visible in the profile render is already present in P01 and is an inherited source artifact; the exact shading cause is not isolated. It is not a P02 improvement or a newly introduced sculpt. Cleanup is deferred to a separately scoped and reviewed pass.

## Review renders

- [Front](P02_front.png) — SHA-256 `AE218C278E150C8917D3804E36AE4E531C22C030D313C960EAA7B437A01E8991`
- [Left profile](P02_left_profile.png) — SHA-256 `7ACB3630DEFB68933E030109F120AD274D5114C6A5575E391E93BE723B9E0A8C`
- [Rear](P02_rear.png) — SHA-256 `0BCA32EC812BE1A284C3009819E83247FA4DECCECCB6BC152FDE9DD0B45BA2E5`

Saved orthographic cameras: front `(0,-4,0.825)`, left profile `(4,0,0.825)`, rear `(0,4,0.825)`; each uses a 2.0 m orthographic scale. Views show the starter A-pose and are appearance checks, not pixel-registered comparisons to the PDF.

## Review gate

- Reviewer: PASS for mechanics and intermediate broad silhouette on exact candidate SHA-256 above. A first zero-change report was withdrawn after same-named Blender library objects were found to have aliased; the corrected comparison used separate Blender processes and exact hashes.
- Planner: ACCEPT as an intermediate checkpoint only; not final Camille acceptance.
- Required report correction applied: the dark posterior thigh/glute patch is inherited P01 artifact; exact shading cause not isolated, not a P02 result; cleanup is deferred.
- Candidate geometry hash remained unchanged by the documentation correction; no mesh correction was requested.
- Remaining: head/neck and arm/hand proportions, face likeness, hair, unitard, materials, animation-ready rig, motion checks, and final anatomical endpoint verification.

