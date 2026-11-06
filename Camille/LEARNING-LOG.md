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
- Observed result: subtle waist, shoulder/chest, pelvis/glute, leg and foot-stance changes. Head/face/ears and arms/hands remain baseline; hair, unitard, materials and rig remain future work. Candidate is not finished or accepted.
- Reviewer report and exact reviewed hash: PASS for candidate SHA-256 `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`; first coordinate comparison was withdrawn because same-named Blender library objects were aliased; corrected independent-process audit confirmed changes.
- Planner disposition (ACCEPT / REJECT / NEEDS USER INPUT): ACCEPT as an intermediate broad-silhouette checkpoint only.
- Numbered corrections: document posterior thigh/glute dark patch as an inherited P01 source artifact with cause not isolated, not a P02 result; defer cleanup. The recommendation was shared with the user and planner before applying.
- Reviewer recheck and exact hash: reviewer PASS applies to the unchanged candidate SHA-256 `51D8C1EF8EEA3F3260DC6B5D0B48C86F69686237FC5775923B2033828174420F`; the P01 shading note was corrected in documentation only.
- What this pass taught us: local shape fields preserve the saved shape-key values and topology, but compare same-named Blender library objects only after verifying data-block identity; separate-process hash-verified comparisons resolved a false zero-change finding. The reference is visual only and artist-selected offsets remain explicitly provisional. The dark posterior patch already exists in P01 and is not evidence of a new sculpt.
- What changes in the next pass: preserve this accepted intermediate checkpoint and proceed to the remaining head/neck, arms/hands, muscle-form, likeness, clothing, materials and rig passes in bounded reviewed iterations.
- Remaining UNKNOWN / NOT_CHECKED items: anatomical endpoints and final stature; head likeness; shoulder/axilla contours; detailed arm/hand proportions; measured circumferences and limb lengths; materials, hair, unitard, rig weights and animation behavior.

