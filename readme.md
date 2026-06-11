# Vecturnal-LS

A single-file HTML tool for generating layered SVG landscapes using Perlin noise.

No dependencies, no build step — a single HTML file you can open locally or deploy to GitHub Pages.

https://stephenmthomas.github.io/vecturnal-ls/


## Features

- **Layered terrain** — stacked closed SVG paths, each with a unique `id`, built from octave Perlin noise
- **Color modes** — flat fill, vertical atmospheric gradient, or radial glow; full control over sky, fog, near, and distant terrain colors with palette presets
- **Voids** — Gaussian-suppressed canyon columns that snake through the layer stack via independent X and Y random walks
- **Animation** — SMIL baked directly into the SVG: per-layer vertical drift, path morphing, or both; stagger controls create rolling wave motion across the stack
- **Export** — downloads a fully self-contained `.svg` file, animations included, playable in any browser or SVG viewer
- **Live preview** — optional real-time regeneration on any control change, seed-stable so terrain shape holds while you tweak

## Usage

Open `terrain-generator.html` in a browser. Adjust sliders, pick a palette, hit **Generate**. Enable animation if wanted, then **Export SVG**.

All settings are reproducible via the seed field.

## Controls

| Section | Key params |
|---|---|
| Layers | Count, spacing, vertical offset, stroke weight, fill toggle |
| Terrain | Roughness, scale X, octaves, persistence, depth spread, horizon tilt |
| Voids | Column count, width (sigma), X-walk (horizontal snake), Y-walk (depth fluctuation) |
| Animate | Mode (drift/morph/both), speed, drift amount, stagger, morph offset |
| Color | Sky, fog, distant, near terrain; gradient style; opacity |
| Canvas | Width, height, path resolution |