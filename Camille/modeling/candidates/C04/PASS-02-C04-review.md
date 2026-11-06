# Camille C04 / P02 Zone 2 chest-ribcage blockout

**Status:** reviewer FAIL and planner REJECT for implementation because the lower deformation fade overlapped the protected C03 waist band. C04 is preserved as failed history and must not be promoted.

## Provenance and approved scope

- Source: `Camille/modeling/candidates/C03/Camille_C03_P02_zone3-waist-refine.blend`
- Source SHA-256: `B404F590559DDC3298038075DB6EA6B2005176015F2A6AE2233B7E6F076DCA7C`
- Candidate: `Camille/modeling/candidates/C04/Camille_C04_P02_zone2-chest-ribcage-blockout.blend`
- Candidate SHA-256: `E17C55B5CF4F003CB5CDBEC526D7916181163D2BA2812758B32C4380CC660AD3`
- Approved visual guide: `C03/P02-zone2-chest-ribcage-redline.png`, SHA-256 `8C0774E844D6C97ED06767373E3D573ED0036CEBC05EB5DC6C75985BCE4B3D44`; companion note SHA-256 `30C3CA76AA353A5B4D5B5E0D8BF59AA8157AEAD63361A7BBE48ECF3C72194609`.
- PDF page 2 remains the sole appearance authority. Images are generated appearance references, not calibrated scans.

## Isolated edit

C04 attempted a soft symmetric field in the upper/mid ribcage/chest area, with artist-selected 2.0% lateral and 2.5% depth controls. The original intent was to fade above the prior C03 waist zone, but that intended boundary was not achieved. Separate-process review found actual C04 changes began at local Z=1.1487 m and produced about 1.312 mm displacement near Z=1.17 m, overlapping C03 waist-band changes that extend to Z=1.1710 m. C04 therefore changed protected waist vertices and failed the approved scope. No Z coordinate changed; other preservation checks passed.

## Preservation and measurement status

- Topology remains 19,158 vertices / 18,486 polygons; evaluated mesh remains 13,380 vertices.
- All saved shape-key values, object transforms/origin, metric units and Mask settings match C03.
- Z coordinates are unchanged; crown, sole and floor datums remain fixed.
- Final anatomical stature remains **UNKNOWN**; no ±0.1 mm stature claim is made.
- Circumferences, body-fat value, and obscured anatomy remain UNKNOWN.

## Review renders

- [Front](P02_front.png) — SHA-256 `51C5E87D09F31890CEADE58A45BFAA0752CE3673872CCF5745E826ACEFC30854`
- [Left profile](P02_left_profile.png) — SHA-256 `AE05E6BB2A41E90E213FE931C31963D5CAEF8ADC76964EAD9B78D63C4580601A`
- [Rear](P02_rear.png) — SHA-256 `D45F4B690C1463D1FE2DDF5CD6A3E10E37765DDCC4D6BD82B63533B9BC90B094`

Views retain the starter A-pose; the PDF arms-at-sides pose differs. Do not use the obscured profile arrow to alter the axilla.

## Review gate

- Reviewer: FAIL on exact candidate SHA-256 `E17C55B5CF4F003CB5CDBEC526D7916181163D2BA2812758B32C4380CC660AD3`; changes started at Z=1.1487 m and overlapped C03’s prior waist edits, which reached Z=1.1710 m.
- Planner: REJECT C04 from promotion; keep as historical failed attempt.
- Correction: new C05 created from C03 with lower fade starting above Z=1.172 m; C03 waist region preserved. C05 passed separate exact-hash review.
- Final stature remains UNKNOWN.
