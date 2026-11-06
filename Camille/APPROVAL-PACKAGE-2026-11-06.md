# Camille approval package — 2026-11-06

**Review state:** The P03 head/face/hair reference set has reviewer PASS and planner ACCEPT. It is awaiting the user's approval before any head, face, or ear geometry edit. This package is not a claim that the whole character is finished or visually accepted.

## What this approval covers

Review the exact P03 board and scope: use the Camille PDF as appearance authority; use only the selected generated 2D face front and profile as supplementary identity cues; intentionally exclude the three-quarter image from this comparison; build on the supplied female starter mesh only; keep accepted body regions and the current skull-crown / stature datum protected; keep the blonde ponytail separate from skull dimensions. No head geometry has been edited.

- [P03 head / face / hair reference board](modeling/candidates/C07/P03-head-face-hair-reference-board.png) — SHA-256 `EDE01B37B6AED722E4A711CBD1B60FC5FD2FD1CE5BF4C095B033E399836931F3`
- [P03 scope, sources, protected regions, and review gate](modeling/candidates/C07/P03-head-face-hair-reference-map.md) — SHA-256 `B95EAED58EBACE27417554CD153F600A5AC62A5C14EE6261D90E899DCA325AD7`
- Reviewer: PASS. Planner: ACCEPT. User approval is the next gate.

## Appearance and modeling sources

- [Approved Camille athletic character sheet PDF](specification/2026-11-05/camille-athletic-character-sheet-2026-11-05.pdf) — SHA-256 `264973DF0712F947917AA6F8EA9E6726D7CB13914B5260FF0350935AC0161A99`. Page 1 gives the design statement/front view; page 2 gives front/profile/rear appearance views; page 6 contains provisional head targets. Generated appearances are not calibrated scans, and their decimals are not micrometer accuracy.
- [Face-reference source notes](specification/2026-11-05/face-references/README.md). Selected P03 images: [front](specification/2026-11-05/face-references/camille-head-front.png), [profile](specification/2026-11-05/face-references/camille-head-profile.png). The [alternate profile](specification/2026-11-05/face-references/camille-head-profile-facing-left.png) and [three-quarter view](specification/2026-11-05/face-references/camille-head-three-quarter.png) remain supplementary; three-quarter is intentionally outside the current comparison. Their loose shoulder-length hairstyle is incidental; PDF ponytail is authoritative.
- Starter model: `source-assets/makehuman/Human_Female_BaseMesh.blend`, SHA-256 `F9AEEE4583248009643A2549CE4F82D1018EDA920F0C3B78EB7D69948F3906A7`. No historical Camille head/body mesh geometry is used.

## Candidate history and review outcomes

| Candidate | Result | Reviewer / planner disposition | Evidence |
|---|---|---|---|
| C01 P01 | Stature-normalized starter checkpoint | PASS; ACCEPT as scale checkpoint only. Final anatomical stature remains UNKNOWN. | [C01 renders](modeling/candidates/C01/P01_front.png), [scale report](modeling/candidates/C01/PASS-01-stature-scale.md) |
| C02 P02 | Broad first athletic silhouette pass | PASS; ACCEPT as intermediate only. | [front](modeling/candidates/C02/P02_front.png), [profile](modeling/candidates/C02/P02_left_profile.png), [rear](modeling/candidates/C02/P02_rear.png), [review](modeling/candidates/C02/PASS-02-C02-review.md) |
| C03 P02 | Waist refinement | PASS; ACCEPT as Zone 3 intermediate only. | [front](modeling/candidates/C03/P02_front.png), [profile](modeling/candidates/C03/P02_left_profile.png), [rear](modeling/candidates/C03/P02_rear.png), [review](modeling/candidates/C03/PASS-02-C03-review.md) |
| C04 P02 | First chest/ribcage boundary attempt | FAIL; REJECTED because it overlapped protected C03 waist edits; retained as history. | [review](modeling/candidates/C04/PASS-02-C04-review.md) |
| C05 P02 | Corrected chest/ribcage boundary | PASS; ACCEPT as intermediate chest/ribcage checkpoint only. | [front](modeling/candidates/C05/P02_front.png), [profile](modeling/candidates/C05/P02_left_profile.png), [rear](modeling/candidates/C05/P02_rear.png), [review](modeling/candidates/C05/PASS-02-C05-review.md) |
| C06 P02 | Pelvis/glute pass | PASS; ACCEPT as intermediate pelvis/glute checkpoint only. Whole-character match not achieved. | [front](modeling/candidates/C06/P02_front.png), [profile](modeling/candidates/C06/P02_left_profile.png), [rear](modeling/candidates/C06/P02_rear.png), [review](modeling/candidates/C06/PASS-02-C06-review.md) |
| C07 P03 | Head/face/hair reference gate, no geometry edit | Reviewer PASS; planner ACCEPT; awaiting user approval. | [board](modeling/candidates/C07/P03-head-face-hair-reference-board.png), [scope note](modeling/candidates/C07/P03-head-face-hair-reference-map.md) |

The user's three-view screenshot was explicitly rejected as an appearance target and is not used for corrections. C06 remains in the starter angled-arm pose, with an unfinished clay head and no ponytail or unitard. The PDF remains the positive target.

## What remains before full character acceptance

Head/face/ears, ponytail construction, athletic likeness refinement, unitard geometry/materials, skin/eye/hair materials, a relaxed presentation pose, Rigify setup and weights, animation deformation review, and final measured stature are not complete. The assigned height is `165.1 cm ±0.1 mm`, floor to anatomical skull vertex excluding hair, but final stature remains **UNKNOWN** until endpoints and the final post-head/post-rig evaluated stack are verified.

## GitHub review location

Public repository: [oppdown/SuperHuman](https://github.com/oppdown/SuperHuman). The current review is [draft PR #6](https://github.com/oppdown/SuperHuman/pull/6). This approval index and the full reviewed C04–C07 materials are part of this draft review update; the PR remains unmerged and in draft while awaiting user approval.

## Approval requested

Approve the exact P03 board and scope note above as the next head/face/ear/ponytail reference gate, or provide corrections. Approval authorizes preparing a fresh head-pass candidate from the supplied starter-derived C06 only after the gate; it does not approve C06 as the final Camille.
