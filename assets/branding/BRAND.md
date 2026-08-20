# Drenyra Guardian Angel — Brand & Banner

> **Normative source:** the Drenyra ecosystem brand contract —
> [`drenyra-ai/contracts/brand-system.md`](https://github.com/arkelythex/drenyra-ai/blob/main/contracts/brand-system.md)
> (v0.3 DRAFT) and canonical tokens at `contracts/brand-system/tokens.json`.
>
> The ecosystem design system is **the Dreamcoder Workbench canonical tokens**:
> Cocoa/Lúcuma Light (warm ivory `#F3EADC`, dark ink `#17120D`) editorial
> surface and Anthracite Steel dark, with cocoa `#824F16` / terracotta
> `#A7471C` accents — readability before decoration. No product invents its
> own palette.

## Regeneration prompt (ChatGPT Images 2.0)

> **Art direction (Dreamcoder Light editorial):** see
> [gpt-image-prompts.md](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md).
> Combine the Shared DNA block (section 4) with the product section below; the
> embedded prompt is the product section only and may trail the canonical file.

The canonical set lives in
[`drenyra-ai/docs/assets/brand/gpt-image-prompts.md`](https://github.com/arkelythex/drenyra-ai/blob/main/docs/assets/brand/gpt-image-prompts.md).
The Guardian Angel prompt is the **frozen review dossier** motif:

```text
Subject: a frozen candidate dossier under independent adversarial review. Place the dossier on the right third as a precise archival folio with a sealed subject hash, cocoa #824F16 structural marks, diagnostic teal #0D4A68 inspection lines, and a small sage #315B31 evidence seal. The object must read as preserved evidence, not a shield, mascot, or approval badge.

Observe the same immutable dossier through two separate review lenses, Judge A and Judge B, with a visible gap between their inspection paths. Their paths converge only in a restrained canonical findings register: corroborated, contradicted, pre-existing, or candidate-caused severe. Add a quiet refutation mark and a bounded correction notation, but never a checkmark or symbol that implies fiscal approval.

Exact, calm, forensic, and editorial — not superhero, fantasy armor, security-software cliché, or generic dashboard UI. The authority boundary should be legible in the composition: Guardian verifies, Drenyra AI runs the candidate lifecycle, and the professional authorizes. Signature detail: two hairline inspection traces meet at the dossier seal while remaining visibly independent.
```

## Validate

```bash
for asset in assets/branding/0{1,2,3,4}-drenyra-guardian-angel-*.png; do
  node ../drenyra-ai/scripts/brand-conformance.mjs "$asset" || exit 1
done
# expect: ✓ <file> (coverage >= 0.92) ... PASS
```

The checker is referenced from the sibling-checkout layout: clone `drenyra-ai`
next to this repository so `../drenyra-ai/scripts/brand-conformance.mjs`
resolves (the same `../<repo>` layout `drenyra-ai/scripts/brand-ecosystem-status.mjs`
assumes) — no host-specific absolute path.

Iterate with the checker's off-palette feedback until every asset reaches
coverage ≥ 0.92. Then `bun run brand:ecosystem` in drenyra-ai must report
this repo `PASS` before brand-system can freeze to v0.3.

## Freeze gate

`brand-system` freezes to v0.3 only when every consuming repo (App Web, Pi,
Engram, Skills, Guardian Angel) passes the same checker on its brand assets in
both themes.
