# Camille P03 head / face / hair reference map

**Status:** Reviewer PASS and planner ACCEPT on this exact board/note pair; no geometry change represented. User review is required before head/face/ear geometry edits.

## Authority and source use

- Primary visual authority: `Camille/specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf`, SHA-256 `264973DF0712F947917AA6F8EA9E6726D7CB13914B5260FF0350935AC0161A99`. Page 1 provides the front appearance; page 2 provides the rear ponytail silhouette; page 6 lists provisional head/face targets and cautions that these are estimates, not scan accuracy.
- Selected supplementary face identity references: front `camille-head-front.png`, SHA-256 `14DE763CC0D700C153B1E3694A1CF24817AC4BAD9B9E33124A804C1905930694`; profile `camille-head-profile.png`, SHA-256 `01E337E05BFA8E7908B3CEBCBFA3440DE08A0F20072610D62BD3E97A6EB7AC2E`. The face-reference README names the three-quarter image as useful for form and identity; it is retained but intentionally excluded from this P03 front/profile comparison. Shoulder-length hair is incidental; PDF ponytail is authoritative.
- Current protected source: C06 pelvis/glute intermediate, SHA-256 `9B11A411F66EBB44DB85688D616B9EF1FC85294551A9BA6E69AA8853DB5706BF`. It supplies only the current mesh boundary and frozen crown datum; no prior Camille mesh geometry is a modeling source.
- User-provided rejected three-view screenshot is excluded from positive design guidance.

## Proposed next edit scope (not yet approved for geometry work)

- Build the head/face blockout and petite ear appearance from the user's supplied female starter mesh only.
- Add a separate blonde ponytail mass following the PDF rear view; it must not alter skull dimensions or the assigned stature endpoint.
- Treat face identity cues as appearance guidance: softly oval face, gentle cheekbones, tapered relaxed jaw, pale blue eyes, light natural brows, straight delicate nose, balanced lips, light freckles, petite close-set ears.
- Use eye centers as the first placement anchors. All feature locations and shapes remain visual estimates. The PDF's 22.9 cm skull-vertex-to-chin value is a working target only, not a micrometer-precision constraint.

## Protected regions and invariants

- Freeze the existing skull-crown point and the assigned 165.1 cm stature datum; hair does not count toward stature.
- Protect neck/body, C03 waist, C05 chest/ribcage, C06 pelvis/glute, shoulders, arms/hands, legs/feet, sole/floor, topology, shape-key values, object transforms/origin, metric units and Mask state.
- Do not reuse historical Camille head/body geometry or introduce any pre-existing model geometry.
- Do not infer hidden anatomy or calibrated facial measurements from the generated images.

## Review gate

The board PNG and this note must receive reviewer feedback, planner disposition, and user review before any head geometry edit. If the skull/face fit conflicts with the frozen crown/stature endpoint, stop and resolve the datum; do not move the crown or sole silently.
