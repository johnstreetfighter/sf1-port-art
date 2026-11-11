# sf1-port-art (private)

The art pack for [sf1-port](https://github.com/johnstreetfighter/sf1-port): the generated poses' pixels, stored in this separate private pack (spec #164, ADR-0006).

- `manifest.json` lists each pose file with its size and CRC-32; the game checks the pack against it.
- `<fighter>/<pose>.png` is an approved pose: an indexed PNG whose indices are the fighter's pens (15 is transparent).
- `candidates/<fighter>/` keeps each PixelLab call's raw candidates (`<job>-<n>.png`) and any touched-up versions, for retries.

What each pose was generated from (references, prompt, seed, cost) and its checksum are in the game repository's `art/generations/` and `art/recipes/`. The game looks for this folder beside the ROM set: `roms\sf` and `roms\sf1-port-art`.

Historical candidate tools find the game checkout when the pack is installed beside the ROM set or cloned beside the game checkout. Set `SF1_PORT_ROOT` to the game checkout to select a different local source.

Keep this repository private.
