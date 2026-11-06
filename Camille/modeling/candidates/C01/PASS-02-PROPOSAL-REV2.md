# Camille C01 / Pass 02 proposal, revision 2 — full-character blockout

**Status: replacement proposal after the user rejected the lower-torso-only scope. No P02 geometry has been edited.** The intended deliverable remains the complete Camille character described in the 2026-11-05 sheet: athletic body, head and face, ears, blonde ponytail, fitted gray unitard, and an animation-ready rig. This pass is the first full-body proportion stage, not the finished character.

## Source and modeling rule

- Work from a new copy of reviewed P01, SHA-256 `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`, which is itself derived from the user's open MakeHuman starter.
- Keep the original open starter and P01 unchanged. Use no pre-existing Camille or other character mesh, sculpt, or rendered model as geometry or as a modeling input. Use only the starter and the supplied 2D character sheet and face-reference images.
- Preserve the five saved shape-key values, metric units, +Z up / -Y forward / +X anatomical left, floor datum, origin, P01 uniform scale, topology, and render/viewport Mask settings. Record any unavoidable change and review it before continuing.

## Pass 02 scope: full-body primary proportions

Adjust broad proportions across the whole starter-derived body: head shape below the crown, neck transition, shoulder girdle, chest and ribcage taper, torso and waist, pelvis and glute/hamstring transition, arms and hands, thighs, calves, ankles, and horizontal foot stance. Work from front, left profile, rear, and approximate top/bottom appearance references as one design family. Use the sheet's joint-center and head landmarks as provisional sculpt starts, then move them to fit the actual mesh. Do not treat image pixels as measured anatomy. The images cannot establish circumferences, body-fat percentage, exact limb lengths or arm span, hidden anatomy, or exact foot length; keep each UNKNOWN until measured on the accepted mesh or supplied as real measurements.

Specific appearance goals in this pass: muscular professional runner; defined but continuous shoulder, trunk, arm, glute, thigh, and calf forms; firm lower abdomen/adductors; fuller posterolateral glute transition; slightly reduced triceps fullness; slender elbows and fingers; trimmed outer-thigh bulges; and the closer-foot stance shown by the latest references. Preserve the requested −2.5 percentage-point body-fat direction as an aesthetic definition cue only. The baseline and absolute body-fat value remain UNKNOWN; do not infer either from clothed/generated references or assign a percentage without direct supplied measurement. Keep bilateral forms mirrored unless a documented visual feature requires otherwise. Do not carve sharp grooves that would read as deformation defects.

The current MakeHuman pose has the arms held outward, while the supplied appearance views show relaxed arms at the sides. Keep shoulder, arm, hand, leg, and stance work in the body pass; this pose difference is a comparison limitation, not a reason to exclude those parts. Compare broad front, profile and rear contours, using the sheet's provisional joint-center targets where pose makes pixel comparison unreliable. Do not back-solve arm span, exact limb lengths, hidden depth, or numeric shoulder/axilla dimensions from the pose-mismatched pixels. Record every occluded or pose-confounded contour as estimated/UNKNOWN and do not claim a pixel-registered scan.

Keep this pass at primary proportions and silhouette. Detailed facial likeness, detailed ear folds, hair geometry, unitard geometry/materials, the Rigify rig, and final export are later named passes in the same complete-character plan below. The head itself is included now for correct overall head-to-body scale and skull-to-chin blockout; use about 229 mm skull-vertex-to-chin only as the sheet's working design anchor.

## Frozen measurement and current stature status

The user-assigned height is 165.1 cm barefoot from floor to anatomical skull vertex, excluding hair, with a selected digital tolerance of ±0.1 mm. P01's evaluated bounds height of `1651.0001590941101 mm` is a scale-normalization diagnostic, not final anatomical acceptance.

A read-only P01 evaluation found provisional low points `6164`, `6165`, `12761`, and `12762` within 0.1 mm of the minimum, at forefoot/toe-contact locations; provisional maximum `881` is near the scalp crown at `1.651000142 m`. These indices are not approved anatomical endpoints, and the low points do not establish a unique sole-contact plane. Anatomical stature therefore remains **UNKNOWN**. During P02, freeze the floor datum and keep provisional crown point `881` at its current world Z; reshape the head only around that fixed point. Preserve foot/sole geometry and every sole point's world Z; if the closer stance is needed, adjust horizontal XY placement and/or yaw only. These constraints preserve the candidate bounds datum but do not verify 165.1 cm stature. Make no height-dependent sculpt decision or height-pass claim. After the full head is fitted and the rig is bound, identify anatomical endpoints and repeat the measurement on the final render-enabled evaluated stack.

## Complete character sequence

1. **P02 — full-body primary proportions:** reshape the starter-derived body across head/body/limbs for the complete athletic silhouette described above; preserve source settings and record front/profile/rear plus top/bottom appearance checks and all pose/reference uncertainties.
2. **P03 — face and ears:** build likeness directly on the starter-derived head using the supplied generated face-reference images and sheet as appearance guides only, not as scans or metric evidence. Establish mirrored pale-blue eye centers first, then eyelids, nose, mouth, jaw/chin, brows and expression. Build both petite ears directly on the head; the smaller/lower/skull-adjacent direction comes only from the approved 2D sheet and generated face references, with no numeric displacement. If placement is unclear, record UNKNOWN and do not guess. No earlier Camille head or ear geometry is reused.
3. **P04 — hair, unitard and appearance:** create a new blonde ponytail and opaque charcoal-gray sleeveless ankle-length athletic unitard as editable geometry fitted to this body. Add a fair neutral-warm skin material, pale-blue eyes, blonde hair material, charcoal suit material, and subtle freckles/surface detail. Preserve bare feet and keep clothing/hair from changing the assigned skull height. Bind new parts to the same final character rig.
4. **P05 — Rigify and animation readiness:** reposition the human metarig to the completed body, generate controls, bind and review weights. Set the closer neutral foot stance while preserving the floor and sole contact; check neutral, arm raise, T/A pose, squat, running stride, wrist and finger curl. Repair visible collapse, twisting, tearing, or foot sliding in new numbered candidates.
5. **P06 — final measurements and handoff:** remeasure assigned height on the complete final evaluated stack, record mesh-derived circumference/landmark values and unknowns, and render the same final mesh from saved orthographic front, profile, rear, true top, and true bottom cameras. Include camera transforms, rig inventory, poses, hashes, and reviewer/planner decisions.

## Review and learning gates

- Before a P02 geometry edit, have the independent reviewer check this exact full-character proposal and the planner disposition their findings. The user must approve the resulting whole-body pass scope.
- For every candidate, store a new `.blend`, source/candidate hashes, saved scene state, comparison views, and a revision-specific reviewer report. The planner records ACCEPT / REJECT / NEEDS USER INPUT and numbered corrections; share the recommendation with the user before applying it. The reviewer then rechecks the corrected exact hash.
- Add the specific observation and consequence for the next pass to `LEARNING-LOG.md`. This is a versioned record of what improved or failed, not model training.

## Superseded scope record

The earlier `PASS-02-PROPOSAL.md` narrowed P02 to waist/pelvis and deferred shoulder, arm, and leg work. The user rejected that scope as inconsistent with the requested complete Camille character. Revision 2 replaces it as the active proposal; the earlier file remains only as history.
