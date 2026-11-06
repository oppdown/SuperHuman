# Candidate C01 / pass 01 - uniform stature scale

**Status: PASS — reviewed intermediate scale checkpoint.** Planner disposition: ACCEPT for advancing to the next bounded modeling step. This is not final character acceptance.

## Provenance

- Source: [`Human_Female_BaseMesh.blend`](../../../source-assets/makehuman/Human_Female_BaseMesh.blend)
- Source SHA-256: `F9AEEE4583248009643A2549CE4F82D1018EDA920F0C3B78EB7D69948F3906A7`
- Candidate: [`Camille_C01_P01_stature-normalized.blend`](Camille_C01_P01_stature-normalized.blend)
- Candidate SHA-256: `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`
- Blender: 5.2.1 LTS; units METRIC, scale length 1.0; frame 1.

## Change

Applied uniform factor `1.0375623371686529` to every stored shape-key coordinate around the assigned floor origin. No local proportion edits or sculpting were made. The five saved shape-key values are unchanged. Object location/rotation/scale remain `(0,0,0) / (0,0,0) / (1,1,1)`. The `Hide helpers` MASK remains enabled in viewport and render, with `body` group, invert false, threshold 0.0.

## Measurement

- Before: evaluated vertical bounds `1.591229693731293 m` under the source-saved shape-key values and render-enabled modifier state.
- After: evaluated vertical bounds `1.6510001590941101 m` (`1651.0001590941101 mm`).
- Difference from assigned 1651.0 mm: `+0.0001590941 mm`; this diagnostic evaluated-bounds value is numerically within ±0.100 mm, but it does **not** verify anatomical stature or pass final acceptance. The mesh is pre-Camille-head-fit and pre-rig.
- Evaluated axis extents (before → after): X `0.9711698294 → 1.0076492379 m`; Y `0.3840658739 → 0.3984922858 m`; Z `1.5912296937 → 1.6510001591 m`. The axes all use the same uniform factor within Blender float precision.
- Evaluated bounds vertices: minimum candidates 6165 and 12762; maximum candidate 881. These IDs are diagnostic bounds candidates only, not verified anatomical endpoint IDs. Final acceptance must be repeated after Camille head fitting and Rigify using the complete render-enabled evaluated stack.
- Topology remains 19,158 vertices / 18,486 polygons. No armature or materials are present yet.

## Visual evidence

- [Front](P01_front.png)
- [Left profile](P01_left_profile.png)
- [Rear](P01_rear.png)
- [Front with endpoint markers](P01_endpoint_front.png)
- [Profile with endpoint markers](P01_endpoint_profile.png)
- [Unscaled source front](baseline_front.png)
- [Unscaled source profile](baseline_left_profile.png)

| Render | SHA-256 |
| --- | --- |
| `P01_front.png` | `F1B31E22386C248DEB07D76083BAE6ED50A72CF1CAE2E1C0EF5342C835356C86` |
| `P01_left_profile.png` | `233F25A4BA75C7035BD3A437B2FC2640D31562E808D3257CB146FD8D32712365` |
| `P01_rear.png` | `258696DC92CC67C76ED7667DF6F57936862CEE28C13C9B483B6DC8DAFAAEF15C` |
| `P01_endpoint_front.png` | `52112247A22E86DA04258B11418C69AE706D2FEF013AA526BB6C5039266746FA` |
| `P01_endpoint_profile.png` | `CDB2B7DF660DFDF257B1ABB89FCCB758A704931DBE29EC6BCBB2B189D4160359` |
| `baseline_front.png` | `33DDE47A9BA7B915F6EDCECC424CD30434CD8BFBE95F56D8B8340F2AB8CD7196` |
| `baseline_left_profile.png` | `2EE95231EBE2B69F25EC23A09C17198453AC691C334D2C4F157D41BC44981167` |

The pass preserves the starter silhouette exactly apart from one common uniform scale. It is not a body-sculpt or likeness pass. The face, athletic refinement, new hair/unitard, rig, and final same-mesh five-view handoff remain outstanding.

## Review gate

- Independent reviewer: **PASS** for this exact candidate SHA-256 `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`. Reviewer confirmed topology, saved shape-key values, transforms, mask settings, reported evaluated height, and preview hashes.
- Planner disposition: **ACCEPT**, limited to a reviewed scale-normalization checkpoint.
- Findings and corrections: none for this checkpoint. The provisional sole and crown vertex IDs do not establish final anatomical endpoints.
- Final stature / character acceptance: **UNKNOWN**. Verify anatomical sole/skull endpoints before stature-dependent sculpt decisions, then re-measure after Camille head fitting and rig binding using the complete final render-enabled evaluated stack; do not claim final ±0.1 mm accuracy from this pass.
- Next step: prepare a bounded Pass 02 body-design proposal for reviewer and planner assessment before making any additional geometry change.
