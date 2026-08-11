# Drenyra Guardian Angel — Brand & Banner

> **Normative source:** the Drenyra ecosystem brand contract —
> [`drenyra-ai/contracts/brand-system.md`](https://github.com/arkelythex/drenyra-ai/blob/main/contracts/brand-system.md)
> (v0.2 DRAFT) and canonical tokens at `contracts/brand-system/tokens.json`.
>
> The ecosystem design system is **the same system as Drenyra apps/web**: dark
> + light themes and the cyan/violet accent system (DTCG token pipeline), with
> the Dreamcoder-inspired compositional language (elevation, aurora glows,
> curved geometry, spark accents). The Guardian Angel must **not** invent its
> own palette — in either theme.

## Regeneration prompt (ChatGPT Images 2.0)
> **Art direction (2026-08-11):** the Shared DNA block was upgraded to the premium minimal-maximal direction — see [creative-brief.md](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/creative-brief.md). Combine the product section below with the **current** Shared DNA from [gpt-image-prompts.md](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md); the embedded prompt is the product section only and may trail the canonical file.

The canonical set lives in
[`drenyra-ai/docs/assets/brand/gpt-image-prompts.md`](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md).
The Guardian Angel prompt is the **twin-lens shield** motif:

```text
Drenyra ecosystem brand banner in the Dreamcoder-inspired visual language:
calm, premium, architectural. Background: deep anthracite-navy canvas #0B0E11
with a faint blueprint grid at ~3% white opacity and a subtle 1% film grain.
Two aurora glows at low intensity (5-8% opacity): cyan #3CE6D8 on the upper
right, violet #9B7FE8 on the lower left. Accent colors allowed ONLY: cyan
#3CE6D8 (lighter #6AEFE4, dimmer #1F8A80), violet #9B7FE8 (lighter #B8A2F0,
dimmer #7B66C0), success green #4ADE94, muted blue-gray #A8B0BC, plus surfaces
#12161B, #1A1F26, #20262E. Composition: a guardian shield formed by two
mirrored curved halves — left cyan #3CE6D8, right violet #9B7FE8 — with a
luminous seam and a checkmark in success green #4ADE94 at its center. Above
the shield, a single lens-shaped beacon (muted blue-gray #A8B0BC with a cyan
#6AEFE4 core) sends two faint concentric ripple arcs downward, with tiny
sparks where the ripples meet the shield's edge. Layered elevation, soft inner
shadows, orbital arcs, no hard rectangles. NO cartoon, NO mascot, NO
photorealism. NO TEXT of any kind. Aspect ratio exactly 1400:460. Keep C2PA
provenance metadata enabled.
```

## Validate

```bash
node ../drenyra-ai/scripts/brand-conformance.mjs \
  assets/branding/drenyra-guardian-angel-banner.png
# expect: ✓ <file> (coverage >= 0.92) ... PASS
```
    
The checker is referenced from the sibling-checkout layout: clone `drenyra-ai`
next to this repository so `../drenyra-ai/scripts/brand-conformance.mjs`
resolves (the same `../<repo>` layout `drenyra-ai/scripts/brand-ecosystem-status.mjs`
assumes) — no host-specific absolute path.
    
Iterate with the checker's off-palette feedback until coverage ≥ 0.92.

## Freeze gate

`brand-system` freezes to v0.3 only when every consuming repo (App Web, Pi,
Engram, Skills, Guardian Angel) passes the same checker on its brand assets in
both themes.
