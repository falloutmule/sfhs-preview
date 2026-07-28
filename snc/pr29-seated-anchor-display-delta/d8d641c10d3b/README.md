# PR #29 seated-anchor display-delta comparison

Immutable Samsung comparison for source commit `d8d641c10d3b63bf9642d42e477b17a0710b8617`.

Open `index.html?heightfield=1&hfcalibration=1&hfseatedanchordisplaydelta=1`.

At equal depth `6.5`, the immutable seated height `0.68` projects to `26.153846` internal pixels over `186` visible source rows: `0.140612` internal pixels/source pixel. The first-order formula `round(target / scale)` produces source deltas `28` and `57`. The comparison then solves the actual renderer source-row rasterization for the opaque shoe component, selecting rows that visibly land at the requested screen-pixel differences:

- A (yellow): source row `182`, actual opaque shoe Y `151`, baseline
- B (orange): source row `159`, actual opaque shoe Y `155`, `+4` internal pixels
- C (magenta): source row `140`, actual opaque shoe Y `159`, `+8` internal pixels

All three have projected ground Y `151`. Their short coloured markers are directly beneath each sitter. DOM labels above the canvas identify A, B, and C without becoming world geometry.

Evidence:

- `evidence/seated-anchor-source-diagnostic.png` — alpha bounds, occupancy, shoe component, detached/shadow tail, and candidate rows.
- `evidence/seated-anchor-equal-depth-browser.png` — full browser screenshot with labels.
- `evidence/seated-anchor-equal-depth-world.png` — world image.
- `evidence/seated-anchor-shoe-crops-4x.png` — nearest-neighbour 4× shoe/ground crops.
- `evidence/seated-anchor-display-delta-browser.json` — actual opaque-shoe measurement, zero browser errors, and zero external requests.

This route is query-only. Standing remains `0.78`; seated remains `0.68`; can work is deferred. No canonical asset, renderer geometry, Gallery data, PR #29, or production deployment changed.
