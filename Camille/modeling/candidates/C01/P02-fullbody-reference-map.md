# Camille C01 / P02 full-body reference map

**Status:** visual scope handoff; not a mesh-edit record. No vertex or scene geometry changes are represented.

## Source hierarchy

- The user-approved character sheet at `Camille/specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf` is the sole appearance target for this pass.
- The front, left-profile and rear panels are the generated appearance references from PDF page 2. They are not registered scans or calibrated orthographic captures.
- P01 is only the starter-derived editable source/checkpoint. Its render is explicitly not a visual target.

## P02 reviewer recommendation order

1. Head/neck mass blockout below the frozen provisional crown; defer face, ears and hair.
2. Athletic shoulder girdle, chest and ribcage. Shoulder roots/axilla remain pose-confounded because the PDF shows arms at sides and P01 has an A-pose.
3. Runner trunk taper and firm lower abdomen. Do not infer circumferences.
4. Fuller glute transition and continuous hamstring fold.
5. Slightly reduced triceps fullness, slender elbows, forearms and fingers.
6. Continuous athletic thigh/calf definition and soft transitions.
7. Closer foot stance through horizontal XY placement and/or yaw only.

## P02 invariants and unknowns

- Keep floor datum, sole geometry and sole-point Z values unchanged; do not alter foot shape.
- Keep the current provisional crown world Z; sculpt the head below/around it without moving the crown in Z.
- Preserve topology, object transforms and origin, saved shape-key values, P01 uniform scale and Mask viewport/render settings.
- Do not claim registered silhouette, exact shoulder/axilla contour, hidden anatomy, exact limb lengths, arm span, circumferences, body-fat percentage, or foot length from these images.
- Stature remains UNKNOWN until anatomical skull and sole endpoints are approved and the completed post-rig evaluated model passes the user's ±0.100 mm tolerance.

## Review gate

The PDF is the approved appearance target; P01 is the editable source only. The reviewer has supplied the sequence above and the planner accepted it with the pose-confounded shoulder/axilla constraint and source hierarchy. Numbered circles indicate sculpt zones and work order only; they are not anatomical points, measurement points, dimensions or registration landmarks. The map is now submitted for exact-artifact reviewer and planner critique before P02 vertex edits.

