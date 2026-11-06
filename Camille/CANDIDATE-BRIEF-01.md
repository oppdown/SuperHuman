# Camille full-body and animation-ready candidate - brief 01

**Status: modeling direction confirmed; P01 is a reviewed scale-normalization checkpoint; P02 scope awaits user approval.** The user directed a from-scratch Camille build using the open starter mesh. The source mesh has not been edited.

## User direction

- Match the Camille body appearance references in the 2026-11-05 character sheet.
- Build Camille's head and body from scratch on the open starter mesh, matching the character sheet and supplied Camille face references.
- Deliver an editable, rigged, animation-ready Blender character.
- Check assigned barefoot stature of 1.651 m to a numeric tolerance of **±0.1 mm**, after the anatomical sole and skull endpoint vertices and measurement state have been verified.

The height tolerance is a geometric acceptance threshold only. It does not make generated reference images or estimated proportions anatomically accurate to 0.1 mm or micrometers.

## Proposed bounded scope

**Model-source rule:** use only the user's open `Human_Female_BaseMesh.blend` as 3D model geometry. Make a versioned working copy and preserve the original. Do not append, join, retopologize, copy, or otherwise use geometry from earlier Camille head/ear files or any other pre-existing character model. Build the head, face, eyes, ears, hair, body, and unitard directly from the starter mesh or as new geometry created in the candidate. Use only the character sheet and the supplied face-reference images as 2D appearance references. The earlier head/ear models and their renders stay in the repository as historical research and are not inputs to this build. The character sheet's front, side and rear views guide body appearance; its top and bottom views remain approximate appearance references. Keep image-derived dimensions and landmarks labeled as estimates unless directly measured from the candidate mesh.

Match the handoff's visual design with a blonde ponytail and opaque charcoal sleeveless unitard, both created as new editable geometry and bound to the character rig. The four face-reference images in [face-references](specification/2026-11-05/face-references/README.md) are generated appearance guides, not calibrated scans. This first candidate does not include cloth or hair simulation, detailed surface textures, or game-engine packaging.

Use the supplied Camille face-reference images for head, eyes, nose, mouth, and expression. The body sheet remains the body appearance authority. If the source views conflict or hide a feature, document the conflict and ask the user before making a consequential choice. Prior head/ear assets and renders are excluded from this candidate's modeling references; the comparison sheet remains historical research only. Ear details are built from scratch and reviewed against the supplied references.

Preserve the source's saved shape-key values as the initial design state; do not reset them to Basis. Record every key and value in each candidate report. For the height check, use the final approved shape-key values, the verified barefoot sole-contact plane, and the anatomical skull-vertex landmark, excluding hair. Measure once after body fitting as a diagnostic, then repeat after all approved head/face/ear work and Rigify binding, with the complete final modifier stack (including the Armature modifier) evaluated in neutral unposed rest state at a declared frame and metric scale length 1.0. Confirm and record that viewport and render modifier enablement agree; compute the acceptance value from the same render-enabled evaluated stack used for final renders. Read evaluated endpoints in world space and calculate `height_mm = (z_skull_world - z_sole_world) * 1000`. Only the final post-head, post-rig result decides acceptance: the full-precision value must satisfy `abs(height_mm - 1651.0) <= 0.100 mm`; apply the threshold before display rounding and report the value to 0.001 mm. Record endpoint names or vertex/group IDs, shape-key values, modifier enablement, evaluated state, candidate hash, and both results. Rerun after any geometry, shape-key, weight, or modifier change. If an anatomical endpoint cannot be uniquely identified through evaluation, mark stature UNKNOWN and do not claim a pass. This is a digital geometry tolerance, not anatomical certainty from images. Do not use the current 1.59123 m bounds value as a substitute.

Add a Rigify-based deformation rig, consistent with the project handoff and installed Blender setup. Confirm plugin and version availability at modeling time. Rig, weight, and pose-check the fitted mesh. Include neutral pose and review captures for raised arms, a forward running stride, hip/knee bend, and elbow/wrist bend. Repair any visible severe pinching, gaps, foot sliding from incorrect rest alignment, or broken control behavior before presenting the candidate for review. This first scope does not include a game-engine export or a polished animation clip.

## Acceptance evidence for this candidate

1. Exact source and candidate `.blend` hashes; source remains unchanged.
2. Stature result within ±0.1 mm of 1.651 m using verified anatomical endpoints in a documented neutral shape-key and modifier state.
3. Same-candidate, matching-scale front, left profile and rear orthographic views, plus true orthographic top and bottom views as specified in the [Blender handoff](specification/2026-11-05/current-references/BLENDER-HANDOFF.md). Record camera matrices and occluded landmarks.
4. Reference comparison notes that separate assigned scale, visual agreement, estimated proportions, and unknown measurements. No claim of micrometer anatomical accuracy.
5. Rig inventory, bind/rest-pose checks, and the specified deformation-pose review captures.
6. Independent reviewer report tied to the exact candidate hash. The planner records ACCEPT / REJECT / NEEDS USER INPUT for each finding and issues numbered corrections; the reviewer checks any corrected hash before promotion.

## Modeling sequence

1. Verify the exact saved source and make a separate candidate copy with a recorded hash.
2. Lock the character-sheet body views and the four supplied face-reference images. Do not use prior head-model renders in this pass.
3. P01 was a diagnostic uniform normalization based on the saved evaluated object bounds. It did not verify the anatomical sole and skull endpoints and is not final 1.651 m acceptance. Before any stature-dependent sculpt decisions, verify and record the anatomical endpoints and measurement state. Reserve the ±0.100 mm acceptance gate for the final post-Camille-head-fit, post-rig candidate evaluated with the complete render-enabled modifier stack; never hide a proportion mismatch with unreviewed axis-only scaling.
4. Sculpt the body directly from the copied starter mesh in bounded passes: silhouette/proportions, then local anatomy. Compare matching front/profile/rear views to the body references after each pass; retain an untouched checkpoint before each pass.
5. Sculpt the head and ears directly on the starter-derived mesh; create eyes, facial details, blonde ponytail and unitard as new geometry. Compare the face guides to the character sheet. The face-reference hairstyle is incidental; use the character sheet's ponytail. Record any conflicting or hidden feature and ask before making a consequential choice. Do not copy or fit existing meshes.
6. Create and bind the Rigify rig to the completed body, head, hair and unitard. Review deformation poses and correct failures on a new numbered candidate.
7. Measure final stature after head work and rig binding with the complete final evaluated modifier stack. Rerun after any later geometry, weight or modifier change. Render the shared-scale orthographic front/profile/rear plus true top/bottom views from that same final candidate. Record matrices, measurements, hashes, PASS/FAIL/UNKNOWN/NOT_CHECKED status, the learning-log entry, and the independent review.

For each bounded pass, the reviewer checks the exact candidate hash, the planner records a disposition and numbered corrections, those corrections go into a new candidate, and the reviewer rechecks the new hash before promotion.

## Approval gate

The user directed a from-scratch full Camille build from the open starter mesh, approved the ±0.1 mm height tolerance, and chose a rigged, animation-ready target. Candidate 01 covers the body, head, facial features, ears, new ponytail and unitard, with the starter-only geometry rule and two height checks (the post-rig ±0.100 mm result is acceptance). Begin only in a separate candidate file; preserve the source and all prior head assets unchanged. If any source ambiguity requires changing this scope, record the issue and ask before proceeding.
