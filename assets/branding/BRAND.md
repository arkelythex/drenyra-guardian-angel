# Drenyra Guardian Angel — Brand & Banner

> **Normative source:** the Drenyra ecosystem brand contract —
> [`drenyra-ai/contracts/brand-system.md`](https://github.com/arkelythex/drenyra-ai/blob/main/contracts/brand-system.md)
> (v0.2 DRAFT) and canonical tokens at `contracts/brand-system/tokens.json`.
>
> The ecosystem design system is **the Dreamcoder Workbench canonical tokens**:
> Cocoa/Lúcuma Light (warm ivory `#F3EADC`, dark ink `#17120D`) editorial
> surface and Anthracite Steel dark, with cocoa `#824F16` / terracotta
> `#A7471C` accents — readability before decoration. No product invents its
> own palette.

## Regeneration prompt (ChatGPT Images 2.0)

> **Art direction (v2, Dreamcoder Light + Black Dark OLED):** see
> [gpt-image-prompts.md](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md).
> Combine the Shared DNA block (section 4) with the product section below; the
> embedded prompt is the product section only and may trail the canonical file.

The canonical set lives in
[`drenyra-ai/docs/assets/brand/gpt-image-prompts.md`](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md).
The Guardian Angel prompt is the **guardian review instrument** motif:

```text
Subject: independent adversarial verification rendered as a guardian review instrument. The hero on the right third is a shield-like precision form composed of two mirrored curved halves in cyan and violet, meeting at a narrow luminous seam. At the seam's center sits a small success-green trust mark, engraved rather than painted.

Hovering above is a single review lens or beacon — refined, optical, and premium — with a dim cyan core. From it descend two faint concentric review ripples that interact with the shield surface, creating tiny spark points where scrutiny meets structure. The whole object should feel like a silent external reviewer watching over the system.

This must feel protective, exact, and calm — not superhero, not fantasy armor, not security-software cliché. Signature detail: the fine engraved ripple traces resolving near the shield edge.
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

Iterate with the checker's off-palette feedback until coverage ≥ 0.92. Then
`bun run brand:ecosystem` in drenyra-ai must report this repo `PASS` before
brand-system can freeze to v0.3.

## Freeze gate

`brand-system` freezes to v0.3 only when every consuming repo (App Web, Pi,
Engram, Skills, Guardian Angel) passes the same checker on its brand assets in
both themes.
