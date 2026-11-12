# Bit-Clip Lab data: Banjo-Kazooie · Xbox 360 (XBLA)

Data files for the [Bit-Clip Lab](https://kweber1.github.io/bitclip-lab/?v=xbox) viewer (the viewer and the tools that make these files are in [kweber1/bitclip-lab](https://github.com/kweber1/bitclip-lab)). Each game version has its own repository so each gets its own 1 GB GitHub Pages site; the viewer loads from all of them on the same `kweber1.github.io` address.

Xbox 360 (XBLA) results for every Banjo-Kazooie room: `data/map<map>.gz.wasm` (gzipped JSON; rooms over 15 MB are split into `map<map>.gz.<n>.wasm` parts, joined in order), listed with their counts in `data/index.json`. Each file has the room's collision (the same level collision as the N64: checked in Xenia) and every Xbox result:

- every crack spot (flat and sloped seams, one per 0.25 cell), found with the Xbox build's own floor-ray maths (it fuses multiply-adds, so many cracks move: some N64 cracks are solid on the Xbox and the Xbox has its own);
- 5 collisions on one update, the full 5-hit hold census with clip odds (`holdsA` rows), and 70 beak-buster dives on every sloped spot, from the Xbox port of the collision resolver (bkgpu_x360) with Xbox timing (2/60 s updates, 0.05 s lag updates, as on N64 NTSC).

Files end in `.wasm` so GitHub Pages serves the gzipped bytes as they are. No game art is published here.
