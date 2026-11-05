# Local scripts omitted from the public snapshot

The source copies of these scripts and input manifests embed absolute user-machine paths. To avoid exposing local folder structure and to avoid shipping scripts that fail on other machines, the public snapshot omits them. Their originals remain in the local project archive unchanged. Each SHA-256 identifies the exact original inspected on 2026-11-05.

| Local source file | SHA-256 | Reason |
|---|---|---|
| `camille-head-blockout-2026-11-03/build_camille_head_v200_substantial_anatomy_pass.py` | `051208b7b6ea04d30c25754dfef53a9109b3106c104b782f6ec6d638b7f99a34` | Hard-coded local workspace path |
| `camille-head-blockout-2026-11-03/build_camille_head_v210_marked_seam_flow.py` | `595155c4e875a7531c2863846045eb1d594f8333ed3669d09040eb9697af0102` | Hard-coded local workspace path |
| `camille-head-blockout-2026-11-03/build_camille_head_v221_no_ears.py` | `28407ae4adbb8c266ffba352b650108ba465d51dbdc0bba8cf35d2f94249e5d5` | Hard-coded local workspace path |
| `camille-head-blockout-2026-11-03/build_camille_head_v222_front_outline_vertex_fit.py` | `0d5bdef878dd7c16af675feb56a0820ca690608925333e2330077ea57fdfddd2` | Hard-coded local workspace path |
| `camille-athlete-2026-11-05/build_character_sheet.py` | `680aa85c655980002307f3632d0f68a45f96898909d54a3acad9a525eb97ca50` | Hard-coded generated-image directory |
| `camille-athlete-2026-11-05/assemble_pack.py` | `8eb26ad34908ecce80c6688eed17656f2298471c677a461e3412e0ef9978cde4` | Its paired pack input contains absolute image paths |
| `camille-athlete-2026-11-05/update_handoff_metadata.py` | `a4d540018c26f5dc6647889a638f6e6a5ca11c3f074959b8dd63a24c3a59e944` | Included only as part of the path-dependent package tooling |
| `camille-athlete-2026-11-05/pack-input.json` | `74c77a5179cadb2f68dccac5e514377a789c96d30d10e8ca627f1322db09d419` | Contains absolute local and generated-image paths |

The public snapshot includes the generated references, prompt text, image hashes, measurements, and selected review evidence. A portable, configurable regeneration workflow can replace these local tools in a later reviewed change.
