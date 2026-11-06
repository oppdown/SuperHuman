# C03 / P02 Zone 2 chest-ribcage reference handoff

**Status:** proposed; pending exact-pair reviewer/planner disposition. No Zone 2 geometry has been edited.

## Source and goal

- Appearance authority: approved Camille athletic character sheet, `Camille/specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf`, page 2. Generated visual references only, not calibrated scans.
- Current editable source: `C03/Camille_C03_P02_zone3-waist-refine.blend`, SHA-256 `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`.
- Redline image: `P02-zone2-chest-ribcage-redline.png`, SHA-256 `8C0774E844D6C97ED06767373E3D573ED0036CEBC05EB5DC6C75985BCE4B3D44`.
- Conceptual zone: upper/mid ribcage and chest appearance below the neck base and above the existing C03 waist band. Fade to zero before the waist band.

## Protected regions and invariants

- Exclude head/neck, shoulders, axillae, arms/hands, C03 lower waist band, pelvis/glutes, legs and feet.
- Preserve topology, shape-key values, object transforms/origin, P01 uniform scale, Mask state, crown world Z, sole/floor Z and all protected regions.
- The A-pose vs PDF arms-at-sides mismatch confounds shoulder/axilla comparison; leave those contours UNKNOWN.
- Use profile only as appearance context where visible. Clothing-covered chest contours and exact zone edges are UNKNOWN. Do not infer measurements, circumferences or body-fat values.
- Open arrows are broad visual tendencies only. They are not anatomical landmarks, boundaries or measurement targets.

## Review gate

Reviewer and planner must disposition this exact image and note before a fresh C04 geometry edit. User-approved PDF scope applies; no new scope approval is needed for this bounded edit.
