# doom-glasses

DOOM running as a web app for smart **display glasses** — a 600×600 dark display with
**D-pad-only** input. Built to be previewed in the Meta Ray-Ban Display Web App Simulator
and, ultimately, loaded on-device.

It's a thin static wrapper: **we do not modify or recompile the game.** A GitHub Actions
workflow assembles the site from a prebuilt WASM DOOM engine + the libre Freedoom IWAD and
publishes it to GitHub Pages.

## What's here
- `index.html` — the glasses shell (600×600), the **control adapter** (D-pad → DOOM keys:
  arrows = move/turn, Select/tap → Fire, Use, Run), and an on-screen **event debugger**
  that logs all input events so the controller can be tuned against real glasses input.
- `.github/workflows/deploy.yml` — fetches the prebuilt engine + Freedoom and deploys to Pages.

## Credits & licenses
- **DOOM engine (WASM):** prebuilt artifacts from
  [VanIseghemThomas/wasmDOOM](https://github.com/VanIseghemThomas/wasmDOOM). The DOOM
  source is GPL (id Software); see that repo for source.
- **Game assets:** [Freedoom](https://freedoom.github.io/) (`freedoom1.wad`), BSD-licensed,
  fully free to redistribute.

No commercial/shareware id WADs are included.
