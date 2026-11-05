# Camille full-body and animation-ready candidate - brief 01

**Status: awaiting user approval before any Blender geometry edit.** This brief records the user's selected output and measurement tolerance and proposes a controlled first modeling scope. It does not authorize editing by itself.

## User direction

- Match the Camille body appearance references in the 2026-11-05 character sheet.
- The completed character should strongly resemble the Camille head work already developed in this project, while fitting the body references.
- Deliver an editable, rigged, animation-ready Blender character.
- Check assigned barefoot stature of 1.651 m to a numeric tolerance of **±0.1 mm**, after the anatomical sole and skull endpoint vertices and measurement state have been verified.

The height tolerance is a geometric acceptance threshold only. It does not make generated reference images or estimated proportions anatomically accurate to 0.1 mm or micrometers.

## Proposed bounded scope

**Model-source rule:** use only the user's open `Human_Female_BaseMesh.blend` as 3D model geometry. Make a versioned working copy and preserve the original. Do not append, join, retopologize, or otherwise use geometry from earlier Camille head/ear files or any other pre-existing character model. Existing Camille head renders may be used only as flat 2D visual references for likeness; they are not geometry sources. The character sheet's front, side and rear views guide body appearance; its top and bottom views remain approximate appearance references. Keep image-derived dimensions and landmarks labeled as estimates unless directly measured from the candidate mesh.

Match the handoff's visual design with an opaque charcoal sleeveless unitard, created as a separate editable mesh and bound to the character rig. The blonde ponytail is deferred until the user selects and approves the head-likeness image set. This first candidate does not include cloth or hair simulation, detailed surface textures, or game-engine packaging.

Use the read-only [head-likeness comparison sheet](research/HEAD-LIKENESS-REFERENCE-SHEET-2026-11-05.md) to select the exact prior Camille head render(s) that guide head proportions and ear design. The body sheet remains the body appearance authority; user-selected prior renders are the visual authority for head silhouette and ear placement, strictly as flat 2D images. The inspected renders are clay blockouts without finished facial detail, so the supplied face references guide eyes, nose, mouth, and expression. The listed head meshes are not finished or approved geometry sources. If selected head renders conflict with the body sheet or face references, document the conflict and ask the user before sculpting the head. Until the user approves named render(s), head sculpting is out of scope; body work may proceed after the candidate brief is approved. Ear details remain separately reviewable and must not be promoted based on an unreviewed mesh filename.

Use the verified barefoot sole-contact plane and anatomical skull-vertex landmark, excluding hair. Measure once after body fitting as a diagnostic, then repeat after Rigify binding and weight setup with the complete final modifier stack, including the Armature modifier, evaluated in neutral unposed rest state at a declared frame, shape keys Basis/default, metric scale length 1.0. Read evaluated endpoints in world space and calculate `height_mm = (z_skull_world - z_sole_world) * 1000`. Only the final post-rig result decides acceptance: the full-precision value must satisfy `abs(height_mm - 1651.0) <= 0.100 mm`; apply the threshold before display rounding and report the value to 0.001 mm. Record endpoint names or vertex/group IDs, evaluated state, candidate hash, and both results. Rerun after any post-measurement change. If an anatomical endpoint cannot be uniquely identified through evaluation, mark stature UNKNOWN and do not claim a pass. This is a digital geometry tolerance, not anatomical certainty from images. Do not use the current 1.59123 m object bounds extent as a substitute.

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
2. Lock the reference set and create the read-only head-likeness sheet; do not import any prior model geometry.
3. Confirm the sole and skull landmarks and the measurement state on the starting mesh. Establish assigned height with uniform scaling only after endpoint verification; never hide a proportion mismatch with unreviewed axis-only scaling.
4. Sculpt the body directly from the copied starter mesh in bounded passes: silhouette and proportions, then local anatomy. Compare matching front/profile/rear views to the body references after each pass; retain an untouched checkpoint before each pass.
5. Create the unitard as new editable geometry and bind it to the body rig. Do not copy existing meshes.
6. Create and bind the Rigify rig. Review deformation poses and correct failures on a new numbered candidate.
7. Measure final stature with the complete post-rig evaluated modifier stack. Render the shared-scale orthographic front/profile/rear plus true top/bottom views from that same candidate. Record matrices, measurements, hashes, PASS/FAIL/UNKNOWN/NOT_CHECKED status, and the independent review.

Head-phase sequence, only after the user approves named image references and a brief revision: compare body-sheet face details against the chosen head renders, resolve any conflict with the user, sculpt head and ears directly on the starter-derived mesh, create eyes/facial details and the ponytail as new geometry, then repeat same-mesh view and rig checks. If no prior render authority is selected, keep all head, face, ear, eye, and ponytail work out of scope; the body-and-unitard candidate is not the final Camille character.

## Approval gate

Before the first geometry edit, the user must approve the named scope: **Camille body-and-unitard animation-ready candidate 01**, including the starter-only geometry rule, new unitard geometry, Rigify rigging, and two height checks with the post-rig ±0.100 mm result as acceptance. This approval allows body-and-unitard work only. The user must also select or explicitly approve named image render(s) from the [head-likeness comparison sheet](research/HEAD-LIKENESS-REFERENCE-SHEET-2026-11-05.md) and approve a revised brief before head, face, ears, eyes, or ponytail work begins. Any conflict between the selected head reference and body-sheet face references must be resolved first. After approval, work begins only in a separate candidate file; the source mesh and all earlier head assets remain unchanged.
