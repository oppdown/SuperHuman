# Camille modeling learning log

This log keeps project-specific findings so each reviewed pass informs the next one. Entries are committed with their candidate evidence to GitHub. This is documented iteration, not model training.

## Per-pass record

Copy this template for each numbered candidate pass. Do not overwrite earlier entries.

### Pass: `CXX - short name`

- Date and author:
- Source `.blend` path and SHA-256:
- Candidate `.blend` path and SHA-256:
- Approved scope and brief revision:
- References used (repository paths and hashes):
- Intended change and reason:
- Measurements and scene/evaluation state:
- Matching views / redline links:
- Observed result:
- Reviewer report and exact reviewed hash:
- Planner disposition (ACCEPT / REJECT / NEEDS USER INPUT):
- Numbered corrections:
- Reviewer recheck and exact hash:
- What this pass taught us:
- What changes in the next pass:
- Remaining UNKNOWN / NOT_CHECKED items:

## Current known lessons

- Do not infer anatomical stature from object bounds. Verify sole and skull endpoints, then use the post-head, post-rig, final-modifier measurement as the acceptance result.
- Reference-image decimals are not anatomical accuracy. Preserve camera alignment, view labels, and uncertainty notes with every comparison.
- Historical Camille head/ear meshes and renders stay outside the geometry and modeling-reference pipeline for this from-scratch build.
