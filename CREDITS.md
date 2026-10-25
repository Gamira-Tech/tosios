# Credits and third-party sources

Gamira client integration: Gamira contributors.

| Component | Authors | Source and licence |
|---|---|---|
| TOSIOS game | Aymeric Chauvin (`halftheopposite`) and contributors | [TOSIOS](https://github.com/halftheopposite/TOSIOS), MIT; retain the original copyright and MIT notice supplied by upstream |
| Colyseus networking | Endel Dreyer and Colyseus contributors | [Colyseus](https://github.com/colyseus/colyseus), MIT |
| PIXI.js renderer | PIXI.js contributors | [PIXI.js](https://github.com/pixijs/pixijs), MIT |
| Dungeon artwork inherited from TOSIOS | `pixel_poem` | Credited in the [upstream README](https://github.com/halftheopposite/TOSIOS#special-thanks); retain that attribution. Exact asset-pack version and asset licence still need verification before public redistribution. |
| Press Start 2P font | Zone38 / upstream font authors | TOSIOS credits [Zone38](http://www.zone38.net/font/) and describes its copy as CC0. Verify the actual font source/version before distribution; similarly named font releases can have different terms. |
| Tiled map editor (creation tool) | Thorbjørn Lindeijer and contributors | [Tiled](https://github.com/mapeditor/tiled) |

The complete JavaScript dependency set is recorded in `TOSIOS/yarn.lock` and the
workspace package manifests. This human-readable list credits principal sources;
installed dependencies retain their own licences and need a distribution notice
inventory when the final build is packaged.

Upstream game and asset copyrights remain with their authors. Gamira's changes
do not relicense upstream content. Preserve original notices when converting the
vendored game into a pinned upstream checkout plus patches.
