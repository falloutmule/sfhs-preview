# PR #29 seated-anchor comparison

Immutable Samsung comparison for source commit `3999a25b3f2a697dce225bfe144f9b587dae8ec9`.

Open `index.html?heightfield=1&hfcalibration=1&hfseatedanchorcomparison=1`.

The seated sprite is shown three times at the same depth and the same immutable world height `0.68`:

- A (yellow): source contact row `182`
- B (orange): source contact row `178`
- C (magenta): source contact row `174`

Each short coloured marker is the projected world ground directly below that instance. There is no global ground line. Standing remains `0.78`, no can is present, and no canonical asset or renderer contract has changed.

`evidence/seated-anchor-source-diagnostic.png` annotates alpha bounds, alpha occupancy, the continuous shoe sole (row `181`), fragmented lower tail/shadow pixels, and all candidate rows. `evidence/seated-anchor-comparison-browser.json` records actual opaque-contact measurements and zero browser errors or external requests.

This preview is review-only. It does not change production or retarget PR #29.
