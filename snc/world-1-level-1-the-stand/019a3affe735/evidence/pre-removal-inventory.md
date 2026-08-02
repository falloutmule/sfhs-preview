# D1 legacy mural pre-removal inventory

Verified from commit `5142e507744c5a9ae7b3f0bf9e62bee45a7469c0` before mutation.

| Authoring record | Runtime prop ID | Position | Runtime texture | Disposition |
| --- | --- | --- | --- | --- |
| `src/levels/district-01-authored.js:163` | `prop-21` | `(5.5, 5.5)` | procedural `mural_panel`, 64x44 | remove D1 placement |
| `src/levels/district-01-authored.js:165` | `prop-23` | `(34.5, 5.5)` | procedural `mural_panel`, 64x44 | remove D1 placement |

The matching Tiled companion records were `Props` objects `42` and `44` in `authoring/levels/district-01/district-01.tmj`.

`mural_panel` remains a shared procedural asset: `src/js/game-15-section-6-procedural-assets.js` registers and draws it, and `src/js/game-09-section-3-city-generation.js` can select it for procedural city districts. It has no import-manifest, generated-runtime registry, or Asset Gallery record, so those are intentionally preserved.

Before count: 46 D1 projected sprite placements = 37 props + 3 recipients + 5 selected cans + 1 portal.

