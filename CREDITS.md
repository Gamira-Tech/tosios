# Credits and third-party sources

Gamira client integration: Gamira contributors.

| Component | Authors | Source and licence |
|---|---|---|
| TOSIOS game | Aymeric Chauvin (`halftheopposite`) and contributors | [TOSIOS](https://github.com/halftheopposite/TOSIOS), MIT; retain the original copyright and MIT notice supplied by upstream |
| Colyseus networking | Endel Dreyer and Colyseus contributors | [Colyseus](https://github.com/colyseus/colyseus), MIT |
| PIXI.js renderer | PIXI.js contributors | [PIXI.js](https://github.com/pixijs/pixijs), MIT |
| Dungeon artwork inherited from TOSIOS | `pixel_poem` | Credited in the [upstream README](https://github.com/halftheopposite/TOSIOS#special-thanks); retain that attribution. Artwork is fetched from upstream and is absent from this patch repository. Its pack/version terms need verification before distributing game assets or builds. |
| Press Start 2P font | Zone38 / upstream font authors | TOSIOS credits [Zone38](http://www.zone38.net/font/) and describes its copy as CC0. The font is fetched from upstream and is absent from this patch repository. Verify the actual font version and supplied terms before distributing game assets or builds. |
| Tiled map editor (creation tool) | Thorbjørn Lindeijer and contributors | [Tiled](https://github.com/mapeditor/tiled) |

The complete JavaScript dependency set is recorded in `TOSIOS/yarn.lock` and the
workspace package manifests. This human-readable list credits principal sources;
installed dependencies retain their own licences and need a distribution notice
inventory when the final build is packaged.

Upstream game and asset copyrights remain with their authors. Gamira's changes
do not relicense upstream content. The full original upstream MIT notice is preserved in `LICENSES/TOSIOS-MIT.txt`.

Full upstream licence notices and terms for Gamira’s changes: [NOTICE.md](NOTICE.md).
