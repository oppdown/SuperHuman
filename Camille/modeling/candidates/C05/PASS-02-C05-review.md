# Camille C05 / P02 Zone 2 chest-ribcage boundary correction

**Status:** reviewer PASS and planner ACCEPT as an intermediate upper-chest/ribcage checkpoint only. C04 remains preserved as the failed boundary-overlap attempt; C05 was created fresh from C03.

## Provenance and approved scope

- Source: `Camille/modeling/candidates/C03/Camille_C03_P02_zone3-waist-refine.blend`, SHA-256 `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`.
- Failed prior candidate retained for history: `C04/Camille_C04_P02_zone2-chest-ribcage-blockout.blend`, SHA-256 `E17C55B5CF4F003CB5CDBEC526D7916181163D2BA2812758B32C4380CC660AD3`.
- Corrected candidate: `Camille/modeling/candidates/C05/Camille_C05_P02_zone2-chest-ribcage-boundary-corrected.blend`, SHA-256 `D784BCADE78C11506763AA5F0ECD676487F823528CF561FA2613DADBD51A1367`.
- Approved redline: `C03/P02-zone2-chest-ribcage-redline.png`, SHA-256 `8C0774E844D6C97ED06767373E3D573ED0036CEBC05EB5DC6C75985BCE4B3D44`; note SHA-256 `30C3CA76AA353A5B4D5B5E0D8BF59AA8157AEAD63361A7BBE48ECF3C72194609`.

## Boundary correction and isolated edit

The first C04 attempt overlapped C03’s waist band and failed review. C05 was created fresh from C03 using the corrected chest-field design first attempted in C04. Its lower fade begins above the C03 affected band and is exactly zero at and below Z=1.172 m. Separate-process coordinate comparison found the lowest changed source Z in the five shape-key blocks between `1.1721067 m` and `1.1726981 m`; C03 waist changes reach `1.1710 m`, leaving a positive gap. The field is exactly zero at and below its 1.172 m lower bound.

Artist-selected visual controls remain 2.0% lateral and 2.5% depth; they are not measurements from the PDF. Across all shape-key blocks, maximum per-vertex shifts are 2.627 mm lateral and 4.442 mm depth. No Z coordinate changed. The profile arm-obscured arrow was not used to infer/change axilla geometry.

## Preservation and measurement status

- Topology remains 19,158 vertices / 18,486 polygons; evaluated mesh remains 13,380 vertices.
- Shape-key values, object transforms/origin, metric units and Mask settings match C03.
- Crown, sole and floor Z datums remain unchanged. Final anatomical stature is **UNKNOWN**; no ±0.1 mm stature claim is made.
- No other regions were edited. Circumferences and obscured anatomy remain UNKNOWN.

## Review renders

- [Front](P02_front.png) — SHA-256 `4A22F0E753977B31D2AA647BD9913715A1CEB7BF51EB9C4B56CB3A72933E9B08`
- [Left profile](P02_left_profile.png) — SHA-256 `11042FAFEE4C72B23AECB9D18F2A7FA42992255F3E711B687084243E2554AFAD`
- [Rear](P02_rear.png) — SHA-256 `7B082E244BB4631F4B201A66B7001F8E0A5C26314BC69396181ACAADCF0278EC`

The starter A-pose differs from the PDF arms-at-sides appearance views; no pixel registration or shoulder/axilla conclusion is made.

## Review gate

- Reviewer: PASS on exact C05 hash above; no overlap with C03 waist edits, no Z changes, and required topology/shape-key/transform/Mask state preserved.
- Planner: ACCEPT as an intermediate chest/ribcage checkpoint only; this is not the completed Camille model.
- C04 remains failed history and is not promoted.
- Next zone requires a separate redline and exact-hash reviewer/planner loop. Final stature remains UNKNOWN.
