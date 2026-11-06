# Camille C01 / Pass 02 proposal — body silhouette and proportions

**Status: proposed only; no Pass 02 geometry edit is authorized yet.** This is the bounded scope to review before the first P02 edit.

## Source and constraints

- Start from a new working copy of reviewed P01: [`Camille_C01_P01_stature-normalized.blend`](Camille_C01_P01_stature-normalized.blend), SHA-256 `E10C4B75185D0FBA1D1969581E17B1DC9F572D4756B36E73A67A2CB49733EF90`.
- P01 itself and the original MakeHuman starter remain untouched.
- Use the character sheet's front, left profile, and rear body views as 2D appearance guidance. Register matching orthographic views and prepare a redline with explicit landmarks before any vertex edits. The outfit is only an image silhouette cue in P02; do not build clothing.
- Do not use any pre-existing Camille model geometry or renders as a modeling input. Face references and the character sheet are 2D only.

## Allowed change

One cohesive silhouette comparison zone only: starter-derived shoulder root/shoulder silhouette, torso and chest volume, waist, and pelvis silhouette. Keep edits broad and localized to the named region/landmark redline. Do not include fine anatomy or surface detail.

## Protected regions and edit boundaries

- Protect the head, face, ears, hair, and neck above the neck base.
- Stop shoulder edits at the shoulder roots/axillae; protect upper arms, arms, hands, and fingers.
- Stop pelvis edits at the hip crease; protect thighs, legs, and feet.
- Do not change the sole-contact geometry, skull/crown geometry, or floor datum.
- Defer arms/hands, legs/feet, head/face/ears/hair, clothing, rigging, and detailed anatomy to separately reviewed candidates.

## Excluded from P02

No head, face, ear, hair, unitard/clothing geometry, armature or weights, materials, topology rebuild, or detailed anatomy. Do not alter stature with axis-only scaling or adjust the P01 uniform factor.

## Pre-edit endpoint gate, frozen state, and measurement

Before any stature-dependent sculpt decision, perform a read-only check and record the anatomical sole-contact plane and skull endpoint IDs, evaluation state, and measurement method. If either endpoint is ambiguous, mark stature UNKNOWN and lock crown, sole, and foot geometry. P02 may still proceed as a relative torso appearance pass, without claiming the assigned 1.651 m stature.

Record and preserve all five saved shape-key values, object transforms, floor/origin datum, P01 uniform factor, topology, and `Hide helpers` MASK settings including viewport and render enablement. Treat the full evaluated bounds only as a diagnostic. Do not report anatomical stature acceptance; the ±0.100 mm gate belongs to the final post-Camille-head-fit, post-rig candidate.

## Review gates

1. User approves this exact P02 scope before the first edit.
2. Complete a registered front/profile/rear view set and redline with named landmarks and camera settings; have reviewer and planner critique and accept that exact redline before any vertex edit.
3. Complete the read-only endpoint gate and record source evaluation state. If endpoint identity is ambiguous, continue only as a relative torso appearance pass with crown/sole/foot protected.
4. Save a fresh versioned P02 candidate and record source/candidate hashes.
5. Render matching front/profile/rear orthographic views with body-reference framing and camera settings recorded. Label image-derived dimensions and landmarks as estimates.
6. Independent reviewer checks the exact candidate hash and returns numbered findings; planner records disposition and corrections; reviewer rechecks any corrected hash before promotion.
7. Log what the review taught the next pass. No further scope is folded into P02.
