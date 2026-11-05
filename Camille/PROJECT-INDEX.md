# Camille character build - project index

Updated 2026-11-05. This index connects the full-body handoff, the open MakeHuman starter mesh, and earlier Camille head/ear research. It records evidence and workflow status; it does not approve a model edit.

## Current body-build scope

The user's Blender screenshot shows Blender 5.2.1 LTS with `Human_Female_BaseMesh.blend` open. The source copy is [`source-assets/makehuman/Human_Female_BaseMesh.blend`](source-assets/makehuman/Human_Female_BaseMesh.blend). This is the intended starter body for Camille's full-body pass. It is distinct from the separately developed Camille head blockout. The saved-file baseline was inspected read-only; see [BASELINE-2026-11-05.md](BASELINE-2026-11-05.md). The Blender screenshot identifies the open file and visible scene; the recorded measurements are from the saved repository copy.

## Current character handoff

- [Athletic character sheet PDF](specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf) is the 12-page visual and modeling/rigging handoff.
- [Blender measurements JSON](specification/2026-11-05/camille-blender-measurements-2026-11-05.json) contains the coordinate system, assigned height, provisional landmark/joint anchors, design directions, and Rigify starter values.
- [Package README](specification/2026-11-05/README-CHARACTER-SHEET.md) summarizes reference status and the requirement to fit one mesh and measure that mesh directly.
- [Current reference package](specification/2026-11-05/current-references/) holds five generated views, the character spec, path-scrubbed prompts and generation records, review coverage, and the [Blender handoff](specification/2026-11-05/current-references/BLENDER-HANDOFF.md).

Evidence classes:

- **Assigned:** fictional adult character; barefoot height 165.1 cm from floor to anatomical skull vertex, excluding hair; floor origin; +Z up, -Y forward, anatomical left +X.
- **Provisional or estimated:** face/head dimensions, ear endpoints, joint coordinates, finger length, torso and limb proportions, and requested athletic form changes. Decimal formatting is for entry convenience, not measurement precision.
- **Visual guidance:** front, left profile, rear, top, and bottom images are generated appearance references, not registered scans of one mesh. Top and bottom are approximate views, not verified orthographic projections.
- **Unknown:** circumferences, absolute body-fat percentage, arm span, and other body measurements that cannot be established from the current images. Replace them with measurements from the fitted mesh or physical measurements where available.

The handoff requires one editable mesh and direct measurements from that mesh. Its final delivery must include matching, shared-scale front/profile/rear orthographic renders and true top/bottom orthographic renders from that same mesh. The top camera looks down -Z and the bottom camera looks up +Z; keep the pose unchanged, hide the floor for the bottom view, use a common orthographic scale, and record/export the camera matrices. Record occluded landmarks as unknown. Treat any required view not yet produced as NOT_CHECKED and hold final acceptance unless the user revises this requirement.

## Related earlier head and ear branch

The selected files in [`research/head-ear/`](research/head-ear/) represent a separate head/ear research branch. They are context for Camille's face and ear design, not components already fitted to the MakeHuman body.

- [v210 review](research/head-ear/REVIEW_v210_ear_anatomy.md) records a split verdict: A/B passed, C remained held, and v210 was not to be promoted without human review.
- [v222 candidate](research/head-ear/Camille_Head_Ear_Fit_Test_v222_front_outline_vertex_fit.blend) and its review renders exist. Its local build script identifies v200 as its source; no v222 reviewer verdict file is included in the inspected source folder. Treat v222 as an unapproved candidate, not an accepted head.
- [v221 no-ear receiver](research/head-ear/Camille_Head_Ear_Receiver_v221_no_ears.blend) and no-ear renders were created later as a receiver for replacement ear work. Its local source script starts from v200 and describes removing the old ear shells and guides while retaining the head, eyes, and mounts. It is a separate branch/artifact, not a successor approval of v222, and is separate from the full-body mesh.
- The original workspace contains additional iterative versions and review records; this repository snapshot includes selected checkpoints and findings, not every intermediate version. Nonportable scripts and path-bearing metadata are omitted, with their filenames and hashes recorded in [`EXCLUDED-LOCAL-SCRIPTS.md`](research/EXCLUDED-LOCAL-SCRIPTS.md). See [`research/head-ear/README.md`](research/head-ear/README.md) for scope.

Do not infer that a newer filename supersedes an unresolved review. When resuming the head branch, connect each edit and review to its source version and hash.

## Gate before modeling

1. Audit the exact starter mesh read-only: object identity, units, transforms, evaluated bounds, floor and skull endpoints, mesh topology, modifiers, materials, shape keys, and any existing rig. Record source hashes.
2. Compare the audit with the assigned scale and current references. Prepare a bounded candidate brief and redline; propose measurable acceptance tolerances only after the baseline is known. Keep geometric precision separate from anatomical accuracy.
3. Get the user's explicit approval of the named candidate scope and tolerances before writing or editing any `.blend` file. Preserve the starter and all existing checkpoints.
4. For each approved candidate, record source and candidate hashes, matching-view evidence, checks marked PASS/FAIL/UNKNOWN/NOT_CHECKED, and a revision-specific reviewer report.
5. The planner reviews the reviewer report and records ACCEPT / REJECT / NEEDS USER INPUT for every finding, with reasons, then issues numbered corrections. Implement accepted corrections only. The reviewer rechecks the exact new candidate hash. Any critical failure or material unknown blocks promotion.
6. Update the measurements and handoff only from the accepted measured mesh. Rigging, animation, or game-engine packaging follows the user's selected delivery target.

No workflow can promise zero mistakes. The project will make errors easier to catch before promotion through isolated versions, explicit measurements, matching views, and a reviewer-to-planner correction record.

## GitHub and asset policy

The public repository is [`oppdown/SuperHuman`](https://github.com/oppdown/SuperHuman), with Camille under this folder and room for other characters. Native `.blend` files use Git LFS. The MakeHuman starter's asset provenance is recorded in [`ASSET-PROVENANCE.md`](source-assets/makehuman/ASSET-PROVENANCE.md); the exact upstream package/version of the local `.blend` is unverified. No blanket reuse license is granted by this repository.

## First next step

Agree the delivery target, endpoint verification method, candidate scope, and numeric acceptance tolerance. The baseline report found a 1.59123 m Z bounds extent versus the 1.651 m assigned stature, but the anatomy endpoints are not identified, so stature compliance remains unknown. Do not begin a body edit or connect the earlier head/ear meshes before those decisions and explicit candidate approval.
