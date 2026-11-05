# Camille head/ear research snapshot

This curated snapshot preserves the source and review context for selected head/ear checkpoints. These files belong to a separate research branch; they are not fitted to the full-body MakeHuman starter.

## Status

- v200 is the source used by the selected v210, v222, and v221 scripts.
- [v210 review](REVIEW_v210_ear_anatomy.md) is a split decision: A/B PASS, C HOLD. Human review was still required before promotion.
- v222 is an unreviewed candidate based on v200. Its review renders are included, but no independent verdict file was found in the source folder. The source build script was kept out of the public snapshot because it contains a machine-specific path; its local original remains unchanged.
- v221 is a later no-ear receiver created separately from v222, also based on v200. The local source script describes removal of the previous pinnae and guides while preserving head, eyes, and mounts. It is not an approval or continuation of v222. The nonportable script was kept out of the public snapshot.

This snapshot includes selected v200, v210, v222, and v221 files to keep key sources and evidence together. The original workspace retains the rest of the iterations, reports, redlines, scripts, and supporting diagnostics. The PDF-generation scripts and path-bearing manifests are also omitted; current images, prompts, hashes, and review records are included. See [`EXCLUDED-LOCAL-SCRIPTS.md`](../EXCLUDED-LOCAL-SCRIPTS.md) for the exact local scripts and hashes. Preserve that archive until a portable regeneration workflow is prepared.
