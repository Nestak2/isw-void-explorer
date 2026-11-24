# ISW imprint of a cosmic void: interactive explorer

**Live page: https://nestak2.github.io/isw-void-explorer/**

An interactive sky map showing how a cosmic void imprints a cold (or hot) spot on the CMB through the integrated Sachs-Wolfe (ISW) effect. Compare standard ΛCDM with the AvERA simulation (Pataki et al. 2025).

## How to use it

- **Move the mouse** (or drag on a touch screen) to steer the void across a simulated 72° × 36° CMB patch. **Click** to lock or release it.
- **Sliders:** void radius, depth (central density contrast), redshift, and an exaggeration factor so the tiny ISW signal is visible against the primordial CMB.
- **Buttons:** switch between ΛCDM and AvERA, between "CMB + ISW" and "ISW only", and between the 1080k and 625k AvERA runs. "New CMB sky" draws a fresh random background.
- The panel reads out the void's distance, angular radius and central ISW temperature in both models. Open **How it's computed** for the equations.

## What it computes

For a compensated Gaussian void in linear theory and the thin-lens approximation,
`ΔT/T ∝ H(z) r0³ δc (1 − f)`, where `f = d ln D / d ln a` is the growth rate. With `f < 1` a void gives a cold spot. With `f > 1` (AvERA above z ≈ 1.7 to 1.9) it gives a hot spot. The expansion history `H(z)`, growth rate `f(z)` and comoving distance `χ(z)` are tabulated in the page for ΛCDM (Planck 2015) and for two AvERA runs. The CMB background is a Gaussian random field from an approximate Planck TT spectrum.

## Limitations

This is a teaching toy, not a precision calculation.

- The CMB spectrum is a rough interpolation, not the Planck best-fit.
- The sky is a flat patch. The page warns when the void is large on the sky.
- The void contrast δc is the same in both models, so differences come only from H(z), f(z) and χ(z).

## Run locally / deploy

Released under the MIT license (see LICENSE). It is a single static file, `index.html`, with no build step. Open it in a browser, or serve it with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root). It loads the Instrument Sans font from Google Fonts and falls back to system fonts offline.
