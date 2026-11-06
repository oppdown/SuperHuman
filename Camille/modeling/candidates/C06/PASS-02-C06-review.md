# Camille C06 / P02 Zone 4 pelvis-glute blockout

**Status:** reviewer PASS and planner ACCEPT as an intermediate pelvis/glute checkpoint only. This is not a whole-character likeness approval and is not the completed Camille.

## Provenance and approved scope

- Source candidate: `Camille/modeling/candidates/C05/Camille_C05_P02_zone2-chest-ribcage-boundary-corrected.blend`; SHA-256 `D784BCADE78C11506763AA5F0ECD676487F823528CF561FA2613DADBD51A1367`.
- Candidate: `Camille/modeling/candidates/C06/Camille_C06_P02_zone4-pelvis-glute-blockout.blend`; SHA-256 `9B11A411F66EBB44DB85688D616B9EF1FC85294551A9BA6E69AA8853DB5706BF`.
- Approved Zone 4 redline: `C05/P02-zone4-pelvis-glute-redline.png`; SHA-256 `96EA333A44FA0DAA6047891F9C079F5007EC4FC55D49ACC675967E01349CEC53`.
- Companion note: `C05/P02-zone4-pelvis-glute-redline.md`; SHA-256 `F9375D4CDB814A432B0A294077F53999DE8CFC3C3FFFFFAAB08DA9780D151CFF`.
- Appearance authority: the approved Camille PDF, page 2. Images are generated appearance references, not calibrated scans.

## Isolated edit and audit

The fresh C06 candidate changes the broad pelvis/glute silhouette and visible posterior glute-to-upper-hamstring transition. Across the five shape-key blocks, changed source vertices span local Z `0.73518–0.92493 m`; the deformation is symmetric and does not move vertices in Z. Maximum component shifts are `2.624 mm` in X and `8.000 mm` in Y; maximum per-vertex vector shift is `8.416 mm`. These are artist-selected controls, not measurements extracted from the PDF.

- Topology: `19,158` vertices / `18,486` polygons; evaluated mesh `13,380` vertices, unchanged from C05.
- Shape-key values, object transforms/origin, metric units, Mask settings, crown Z, sole/floor Z and all protected zones match C05.
- The C03 waist and C05 chest/ribcage remain protected. Head/neck, shoulders/axillae, arms/hands, lower legs and feet are unchanged.
- The inherited dark posterior patch is visible in the render; it was present in P01 and remains excluded because its cause has not been isolated.

## Review views

- [Front](P02_front.png) — SHA-256 `DB723FEA00DC167F5E67218AAC5A630901BA11939975E62BEFEDE963B7F1B493`
- [Left profile](P02_left_profile.png) — SHA-256 `F78620F7E145B1028C083ACC3DC9C1A32C4F722B8EC6CD3B2B6B6519EE861F60`
- [Rear](P02_rear.png) — SHA-256 `E37E3A90730A01527F625D186C9822D3CB49F724AF9A16B6C16EFDFBD346158B`

## Whole-character status and disposition

The user confirmed the PDF is the positive target and the supplied three-view screenshot is not. The screenshot is excluded from design guidance. The C06 render remains in the starter angled-arm pose, with an unfinished clay head and no unitard or hair; reviewer confirmed C06 should be retained only as a local Zone 4 intermediate. It does not establish whole-character likeness.

- Reviewer: PASS on the exact C06 candidate and the three hashes above.
- Planner: ACCEPT as a Zone 4 intermediate checkpoint only; retain unchanged.
- Stature: **UNKNOWN** until anatomical endpoints are approved and the final post-head/post-rig stack is measured against the assigned `165.1 cm ±0.1 mm` target.
- Not checked: final face/head/ears, ponytail, unitard/materials, rig weights, animation behavior, final appearance pose, and final post-rig stature.
