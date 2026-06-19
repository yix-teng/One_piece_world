# 🏴‍☠️ Grand Line Explorer

A mobile, portrait-mode **3D walking simulator** set in the world of *One Piece*.
You play as **Luffy**, exploring a Foosha-style island — palm beaches, a village
with a windmill, a lighthouse, and the Thousand Sunny moored offshore. Find all
the treasure chests scattered across the island!

> Fan-made, non-commercial tribute. *One Piece* is © Eiichiro Oda / Shueisha / Toei.

## ▶️ Play

It's a single self-contained file. Just open **`index.html`** in a browser.

- **On your phone:** host the folder somewhere (GitHub Pages, or any static
  host) and open it in mobile Safari/Chrome, held **upright (portrait)**.
- **Local test on a computer:**
  ```bash
  python3 -m http.server 8000
  # then visit http://localhost:8000
  ```

The game uses [three.js](https://threejs.org) loaded from a CDN, so the **first
load needs an internet connection** (it caches after that).

## 🎮 Controls

| Control | Action |
|---|---|
| **Floating D-Pad** (bottom-left) | Walk Luffy around — drag in any direction |
| **DASH** button | Hold to sprint |
| **JUMP** button | Gum-Gum jump |
| Keyboard (desktop) | `WASD` / arrows to move, `Shift` to dash, `Space` to jump |

Movement is camera-relative and the view is **3rd person** — the camera trails
behind Luffy as he turns.

## 🗺️ Goal

Roam the island and collect all **10 treasure chests** (the floating gold coins).
Collect them all to become King of the Pirates!

## 🛠️ How it's built

Everything is rendered with **three.js primitives** — no external image assets
are fetched at runtime, so the world (Luffy's straw hat, the Sunny's lion
figurehead, the windmill village, animated ocean, drifting clouds) is fully
procedural and works offline once the library is cached. Single `index.html`,
no build step.
