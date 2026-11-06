# Camille modeling learning log

This log keeps project-specific findings so each reviewed pass informs the next one. Entries are committed with their candidate evidence to GitHub. This is documented iteration, not model training.

## Per-pass record

Copy this template for each numbered candidate pass. Do not overwrite earlier entries.

### Pass: `CXX - short name`

- Date and author:
- Source `.blend` path and SHA-256:
- Candidate `.blend` path and SHA-256:
- Approved scope and brief revision:
- References used (repository paths and hashes):
- Intended change and reason:
- Measurements and scene/evaluation state:
- Matching views / redline links:
- Observed result:
- Reviewer report and exact reviewed hash:
- Planner disposition (ACCEPT / REJECT / NEEDS USER INPUT):
- Numbered corrections:
- Reviewer recheck and exact hash:
- What this pass taught us:
- What changes in the next pass:
- Remaining UNKNOWN / NOT_CHECKED items:

## Current known lessons

- Do not infer anatomical stature from object bounds. Verify sole and skull endpoints, then use the post-head, post-rig, final-modifier measurement as the acceptance result.
- Record saved shape-key values and modifier evaluation state before comparing any bounds; the active source values and helper mask materially change evaluated stature.
- Record modifier enablement for viewport and render; the final measurement and evidence renders must evaluate the same stack.
- Reference-image decimals are not anatomical accuracy. Preserve camera alignment, view labels, and uncertainty notes with every comparison.
- Historical Camille head/ear meshes and renders stay outside the geometry and modeling-reference pipeline for this from-scratch build.

## Completed passes

### Pass: `C01 P01 - stature normalization`

- Date and author: 2026-11-05; Codex modeling pass with independent reviewer and planner.
- Source `.blend` path and SHA-256: `source-assets/makehuman/Human_Female_BaseMesh.blend`; `F9AEEE4583248009643A2549CE4F82D1018EDA920F0C3B78EB7D69948F3906A7`.
- Candidate `.blend` path and SHA-256: `Camille/modeling/candidates/C01/Camille_C01_P01_stature-normalized.blend`; `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`.
- Approved scope and brief revision: one uniform scale about the assigned floor origin; C01 brief; no local proportion or sculpt changes.
- References used: audited starter scene and assigned 1651.0 mm height. No earlier Camille mesh or render geometry used.
- Intended change and reason: normalize the starter's evaluated height to the assigned digital stature before anatomy work.
- Measurements and scene/evaluation state: source evaluated Z extent `1.591229693731293 m`; candidate `1.6510001590941101 m` (`1651.0001590941101 mm`), `+0.0001590941 mm` from target. Saved shape-key values, object transforms, mask settings and topology preserved. The endpoints remain provisional.
- Matching views / redline links: [front](modeling/candidates/C01/P01_front.png), [left profile](modeling/candidates/C01/P01_left_profile.png), [rear](modeling/candidates/C01/P01_rear.png), [front endpoint diagnostic](modeling/candidates/C01/P01_endpoint_front.png), [profile endpoint diagnostic](modeling/candidates/C01/P01_endpoint_profile.png).
- Observed result: pure uniform scale; starter silhouette and proportions unchanged. No armature, materials, face/head work, athletic refinement, hair, or unitard yet.
- Reviewer report and exact reviewed hash: PASS for candidate SHA-256 `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`; reviewer confirmed preservation checks, reported scale and preview hashes. Final anatomical height remains UNKNOWN until endpoints and final post-rig evaluated stack are checked.
- Planner disposition: ACCEPT only as a reviewed scale-normalization checkpoint.
- Numbered corrections: none for P01.
- Reviewer recheck and exact hash: no correction was requested; reviewer disposition applies to the exact candidate hash above.
- What this pass taught us: uniform normalization can meet the numerical tolerance on the saved pre-head/pre-rig evaluated state, but it cannot establish final anatomical height while endpoint identity is provisional.
- What changes in the next pass: submit a bounded body-design proposal for reviewer and planner assessment before any new geometry edit.
- Remaining UNKNOWN / NOT_CHECKED items: anatomical endpoints; final post-head/post-rig height; body likeness; face/head/ear fit; rig and animation behavior; materials and outfit; final five-view handoff.

### Pass: `C02 P02 - full-body silhouette blockout` (reviewed intermediate)

- Date and author: 2026-11-05; Codex modeling pass with independent reviewer and planner.
- Source `.blend` path and SHA-256: `Camille/modeling/candidates/C01/Camille_C01_P01_stature-normalized.blend`; `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`.
- Candidate `.blend` path and SHA-256: `Camille/modeling/candidates/C02/Camille_C02_P02_full-body-athletic-blockout.blend`; `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`.
- Approved scope and brief revision: PDF-driven full-body P02 per `C01/PASS-02-PROPOSAL-REV2.md` and `C01/P02-fullbody-reference-map.png`; reference-map exact hash `70EDA4BD2C6CCC45E94FC3E93D86474FDC4B9C9D13809377D7D92B45DE74EA7B`.
- References used: approved PDF `Camille/specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf` (SHA-256 `264973DF0712F947917AA6F8EA9E6726D7CB13914B5260FF0350935AC0161A99`); no prior Camille geometry.
- Intended change and reason: introduce a first modest symmetric athletic silhouette adjustment while preserving the starter-derived topology and scene state.
- Measurements and scene/evaluation state: topology 19,158 vertices / 18,486 polygons; stored shape-key values, object transforms, metric units, Mask viewport/render state, and all vertex Z coordinates preserved. Applied 18 mm per-foot horizontal convergence at low Z as an artist-selected provisional value, not a PDF measurement. Stature remains UNKNOWN.
- Matching views / redline links: `C02/P02_front.png`, `C02/P02_left_profile.png`, `C02/P02_rear.png`; hashed in `C02/PASS-02-C02-review.md`. P01 A-pose differs from PDF arms-at-sides; no pixel-registration claim.
- Observed result: subtle waist, shoulder/chest, pelvis/glute, leg and foot-stance changes. Head/face/ears and arms/hands remain baseline; hair, unitard, materials and rig remain future work. Candidate is not finished; accepted as an intermediate checkpoint only.
- Reviewer report and exact reviewed hash: PASS for candidate SHA-256 `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`; first coordinate comparison was withdrawn because same-named Blender library objects were aliased; corrected independent-process audit confirmed changes.
- Planner disposition (ACCEPT / REJECT / NEEDS USER INPUT): ACCEPT as an intermediate broad-silhouette checkpoint only.
- Numbered corrections: document posterior thigh/glute dark patch as an inherited P01 source artifact with cause not isolated, not a P02 result; defer cleanup. The recommendation was shared with the user and planner before applying.
- Reviewer recheck and exact hash: reviewer PASS applies to the unchanged candidate SHA-256 `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`; the P01 shading note was corrected in documentation only.
- What this pass taught us: local shape fields preserve the saved shape-key values and topology, but compare same-named Blender library objects only after verifying data-block identity; separate-process hash-verified comparisons resolved a false zero-change finding. The reference is visual only and artist-selected offsets remain explicitly provisional. The dark posterior patch already exists in P01 and is not evidence of a new sculpt.
- What changes in the next pass: preserve this accepted intermediate checkpoint and proceed to the remaining head/neck, arms/hands, muscle-form, likeness, clothing, materials and rig passes in bounded reviewed iterations.
- Remaining UNKNOWN / NOT_CHECKED items: anatomical endpoints and final stature; head likeness; shoulder/axilla contours; detailed arm/hand proportions; measured circumferences and limb lengths; materials, hair, unitard, rig weights and animation behavior.



### Pass: `C03 P02 - Zone 3 waist refinement` (reviewed intermediate)

- Date and author: 2026-11-05; Codex modeling pass with independent reviewer and planner.
- Source `.blend` path and SHA-256: `Camille/modeling/candidates/C02/Camille_C02_P02_full-body-athletic-blockout.blend`; `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`.
- Candidate `.blend` path and SHA-256: `Camille/modeling/candidates/C03/Camille_C03_P02_zone3-waist-refine.blend`; `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`.
- Approved scope: isolated trunk/waist/lower-abdomen zone with open-arrow redline `C02/P02-zone3-reference-redline.png` SHA-256 `4664F9653FEFE1BFF76DC9A00ABA3A615D95CA344211E63B0770F65D973AB85F`; paired note SHA-256 `3508FC350F517CC62ECC645BA78279C4F757F74BF6B84EF4E8EECD7F63FA7531`.
- Intended change and reason: very modest additional waist taper and anterior depth refinement within a bounded trunk zone; exact generated-reference dimensions were not inferred.
- Scene/evaluation state: 19,158 vertices / 18,486 polygons, unchanged shape-key values, identity transforms, Mask state preserved, zero Z-coordinate changes. Max per-vertex displacement was 3.661 mm lateral and 1.835 mm anterior by artist-selected field parameters. Stature remains UNKNOWN.
- Matching views: `C03/P02_front.png` SHA-256 `1F8D5E4C232AE9EA12275E4C82208F7A42C3BE918717EE8B1AB78965B7D565C8`; profile `43D27CB56AE48A7802ABA374A80DC65D8660AA6071CBC79970A567B2AA3BFD7D`; rear `688C7C02C43B4B951B8D8BA9F526EFC04CED6C5B09054CD699716D05C221E024`.
- Reviewer report and exact hash: PASS for candidate SHA-256 `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`; no over-carving observed.
- Planner disposition: ACCEPT as a Zone 3 intermediate checkpoint only.
- Corrections: none requested. Next zone requires its own bounded redline and reviewer/planner loop.
- What this pass taught us: small symmetric deformation fields can make a controlled waist refinement while preserving vertical datums, but visible appearance remains subtle at this stage and does not establish final likeness or stature.
- Remaining UNKNOWN / NOT_CHECKED: final endpoints and stature; head likeness; shoulders/axilla and arms/hands; circumferences and hidden anatomy; hair/unitard/materials; rig and motion behavior.


### Pass: `C04 P02 - Zone 2 first attempt` (failed; retained as history)

- Date and author: 2026-11-05; Codex modeling pass with independent reviewer and planner.
- Source `.blend`: `Camille/modeling/candidates/C03/Camille_C03_P02_zone3-waist-refine.blend`; `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`.
- Failed candidate `.blend`: `Camille/modeling/candidates/C04/Camille_C04_P02_zone2-chest-ribcage-blockout.blend`; `E17C55B5CF4F003CB5CDBEC526D7916181163D2BA2812758B32C4380CC660AD3`.
- Review: FAIL. C03 waist changes extended to Z=1.1710 m; C04 changes began at Z=1.1487 m, overlapping the protected Zone 3 band. Other preservation checks passed, but this boundary violation blocked acceptance.
- Planner disposition: REJECT C04 for promotion and require a new numbered candidate; C04 remains unchanged history.
- Learning: a gaussian/fade boundary must be compared to the actual prior edited-Z extent before changing an adjacent region.

### Pass: `C05 P02 - Zone 2 boundary-corrected chest/ribcage` (reviewed intermediate)

- Date and author: 2026-11-05; Codex modeling pass with independent reviewer and planner.
- Source `.blend`: `Camille/modeling/candidates/C03/Camille_C03_P02_zone3-waist-refine.blend`; `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`.
- Candidate `.blend`: `Camille/modeling/candidates/C05/Camille_C05_P02_zone2-chest-ribcage-boundary-corrected.blend`; `D784BCADE78C11506763AA5F0ECD676487F823528CF561FA2613DADBD51A1367`.
- Approved scope: upper/mid chest/ribcage redline `C03/P02-zone2-chest-ribcage-redline.png`; reviewer/planner accepted exact pair before edits.
- Review: PASS. C03 waist changed points end at Z=1.1710 m; C05 changed points begin at or above Z=1.1721 m. No shared changed vertices, Z movement, topology/key-value/transform/Mask change, or axilla edits observed.
- Planner disposition: ACCEPT as an intermediate upper-chest/ribcage checkpoint only.
- What this pass taught us: adjacent sculpt fields need a measurable zero-change gap and a direct changed-vertex overlap check; preserve failed candidates as history and make corrections in new numbered files.
- Remaining UNKNOWN / NOT_CHECKED: final stature, hidden anatomy, circumferences, face likeness, outfit, rig and motion checks.

### Pass: `C06 P02 - Zone 4 pelvis/glute blockout` (reviewed intermediate)

- Date and author: 2026-11-05; Codex modeling pass with independent reviewer and planner.
- Source `.blend`: `Camille/modeling/candidates/C05/Camille_C05_P02_zone2-chest-ribcage-boundary-corrected.blend`; `D784BCADE78C11506763AA5F0ECD676487F823528CF561FA2613DADBD51A1367`.
- Candidate `.blend`: `Camille/modeling/candidates/C06/Camille_C06_P02_zone4-pelvis-glute-blockout.blend`; `9B11A411F66EBB44DB85688D616B9EF1FC85294551A9BA6E69AA8853DB5706BF`.
- Scope: reviewed Zone 4 pelvis/glute redline and note in C05. The front boundary remains approximate; only visible posterior profile contour is used. No hidden anatomy or measurements inferred.
- Audit: changed source vertices across five shape-key blocks are confined to local Z `0.73518–0.92493 m`, symmetric, with zero Z displacement. Maximum X/Y components are `2.624/8.000 mm`; maximum vertex shift is `8.416 mm`. Topology, key values, transforms, Mask, metric units and all protected body zones match C05.
- Review views: C06 `P02_front.png`, `P02_left_profile.png`, and `P02_rear.png`; exact hashes recorded in `C06/PASS-02-C06-review.md`.
- Reviewer: PASS on the exact candidate hash; smooth contour change in the approved region. The inherited posterior patch remains excluded from sculpting.
- Planner: ACCEPT as an intermediate Zone 4 checkpoint only; retain C06 unchanged.
- Whole-character gap: C06 remains in the starter angled-arm pose, with unfinished clay head, no ponytail or unitard. User explicitly confirmed PDF as positive appearance target and rejected screenshot as design guidance.
- Stature remains UNKNOWN. Face/head/ears, ponytail, unitard/materials, rig, animation behavior, relaxed presentation pose, and final post-rig stature remain future work.

### Pass: `C07 P03 - head/face/hair reference gate` (approved by reviewer/planner; awaiting user review)

- No geometry edit. The PDF remains appearance authority; the rejected three-view screenshot and historical Camille geometry are excluded.
- Exact board: `Camille/modeling/candidates/C07/P03-head-face-hair-reference-board.png`; SHA-256 `EDE01B37B6AED722E4A711CBD1B60FC5FD2FD1CE5BF4C095B033E399836931F3`.
- Exact scope note: `Camille/modeling/candidates/C07/P03-head-face-hair-reference-map.md`; SHA-256 `B95EAED58EBACE27417554CD153F600A5AC62A5C14EE6261D90E899DCA325AD7`.
- Reviewer: PASS; planner: ACCEPT the exact pair. The face reference three-quarter image is retained but explicitly excluded from this front/profile comparison.
- User approval of this exact reference set is the gate before any head, face, or ear geometry work.
- If face fit conflicts with the frozen crown/stature datum, stop and resolve the conflict. No crown/sole movement, hidden anatomy inference, or micrometer-precision face claim is authorized by the visual references.
