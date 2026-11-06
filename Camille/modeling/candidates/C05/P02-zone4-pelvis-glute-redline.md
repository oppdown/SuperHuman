# C05 / P02 Zone 4 pelvis-glute-hamstring reference handoff

**Status:** exact redline and note received reviewer PASS and planner ACCEPT before edits. C06 implements this scope as a reviewed intermediate; see `../C06/PASS-02-C06-review.md`.

## Source and goal

- Appearance authority: approved Camille athletic character sheet, page 2 of `Camille/specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf`. Generated appearance views only; not calibrated scans.
- Current editable source: `C05/Camille_C05_P02_zone2-chest-ribcage-boundary-corrected.blend`, SHA-256 `D784BCADE78C11506763AA5F0ECD676487F823528CF561FA2613DADBD51A1367`.
- Redline image: `P02-zone4-pelvis-glute-redline.png`, SHA-256 `96EA333A44FA0DAA6047891F9C079F5007EC4FC55D49ACC675967E01349CEC53`.
- Conceptual cue: broad pelvis/glute outer silhouette and visible glute-to-hamstring transition, using front/rear appearance and only unobscured posterior profile silhouette.

## Protected regions and invariants

- Preserve the entire C03 waist band and C05 chest/ribcage; exclude head/neck, shoulders/axillae, arms/hands, legs below the transition, and feet.
- Preserve topology, shape-key values, transforms/origin, metric units, Mask state, crown world Z, sole/floor Z, and all protected regions.
- Unitard clothing hides anatomy. Do not infer glute volume percentage, circumference, exact fold placement, or hidden anatomy. Clothing-covered boundaries remain UNKNOWN.
- The dark posterior patch is already present in P01 as an inherited source artifact; its exact shading cause is not isolated. It is not an edit target.
- Open arrows are broad appearance tendencies only, not anatomical boundaries, dimensions, or measurement points.

## Review gate

- Reviewer: PASS on exact image/note hashes above; front cue remains approximate, profile is limited to visible posterior contour, and no measurements or hidden anatomy are inferred.
- Planner: ACCEPT this bounded scope for a fresh edit from C05.
- User-approved PDF scope applies. C06 is a reviewed intermediate, not whole-character approval.
