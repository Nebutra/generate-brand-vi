---
name: generate-brand-kit
description: Create or migrate a complete brand kit and production asset pipeline for a repo, app, system, product, or campaign. Use when Codex is asked to design a brand/VI/visual identity, replace an existing brand, generate logo/icon/app-icon/hero/social/background assets, build image-generation DAGs and prompts, translate abstract brand philosophy into product-consumable files, audit old brand assets, or clean up legacy/rejected visual material.
---

# Generate Brand Kit

## Core Idea

Create brand systems that behave like water: take the shape of the project, product surface, culture, and philosophy before hardening into assets. Do not start with a logo prompt. Start with the target structure, existing repo conventions, product consumption paths, and the brand's meaning.

## Workflow

1. **Read the existing system first.**
   - Inspect repo style docs, asset folders, app configs, icon build scripts, locale/product names, README/social images, and current brand terms.
   - If the repo is unfamiliar, run `scripts/scan_brand_assets.py <repo> --brand-term <old> --brand-term <new>` for an inventory seed.

2. **Define the target material list before generating.**
   - Create an inventory of every slot the product consumes: SVG, PNG, ICNS, ICO, app config icons, favicons, splash images, README/hero/social backgrounds, mobile adaptive icons, in-app logos, docs images, and generated source masters.
   - Use `references/asset-taxonomy.md` for common slots and sizes.
   - Identify build commands and generated outputs. Do not replace only the visible logo while leaving compiled assets stale.

3. **Distill the brand philosophy into VI rules.**
   - Abstract the brand IP from the product's business scenario — what the product does or means for its buyers. Never promote an incidental metaphor (from internal docs, the agent's own process language, or this skill's documentation) into the client brand's IP.
   - Name, language variants, tone, design philosophy, cultural references, material metaphors, shape grammar, palette, typography, imagery, motion if relevant, and negative constraints.
   - Position against the current aesthetic landscape with `references/trends-2026.md`; ground craft decisions in `references/design-theory.md`; pull stage-appropriate visual references via `references/inspiration-sources.md`.
   - Treat user aesthetic direction as product strategy, not decoration.
   - Write or update a `visual-identity.md` / `brand-kit-inventory.md` style document before mass generation.
   - Use `references/workflow.md` for the decision gates.

4. **Design the generation DAG deliberately.**
   - Prefer a serial DAG for consistency: foundation boards -> symbol motifs -> core mark -> production-clean mark -> variants -> product outputs -> proof sheets.
   - Put shared references early in the DAG when object/shape consistency matters. Do not rely on prompt adjectives alone.
   - If the user rejects hard shape guides, make prompts explicit enough to constrain form, composition, material, and banned readings.
   - Use `references/generation-dag.md` and `references/prompt-patterns.md`.

5. **Generate, judge, and promote assets.**
   - Use the available image generation/editing skill or tool when raster generation is needed.
   - Promote only approved masters into an `approved/` or equivalent stable directory.
   - Keep rejected explorations out of the product path; remove or quarantine them so future agents cannot accidentally consume them.

6. **Convert into product-ready assets.**
   - Hand-vectorize or edit SVG for production marks when raster output is not enough.
   - Export all required bitmap sizes and platform formats. Use existing repo icon scripts when present.
   - For desktop icons, verify alpha/transparent intent; for mobile icons, respect platform-specific opaque/adaptive requirements.

7. **Integrate and verify.**
   - Replace source assets, generated assets, app config references, in-app components, documentation, and localized product names.
   - Run relevant asset scripts, type checks, tests, JSON validation, image/file checks, and legacy scans.
   - Visually inspect critical assets in context, especially dock/app icons and first-run/empty states.

8. **Commit only after hygiene.**
   - Scan for legacy names, rejected paths, stale generated outputs, and old remote/upstream references when a full brand migration is requested.
   - If committing, stage only intended files and summarize verification honestly.

## Useful Resources

- `scripts/scan_brand_assets.py`: inventory likely brand files and text hits in a repo.
- `scripts/create_brand_kit_scaffold.py`: create a neutral brand-kit scaffold in a target repo.
- `references/workflow.md`: detailed process, decision gates, and “water-shape” interpretation.
- `references/asset-taxonomy.md`: product-consumable asset checklist.
- `references/generation-dag.md`: DAG design and consistency patterns.
- `references/prompt-patterns.md`: prompt architecture for professional visual generation.
- `references/validation.md`: QA, integration, and legacy cleanup checks.
- `references/trends-2026.md`: current aesthetic trends — rising, falling, and trend-tracking sources.
- `references/design-theory.md`: durable identity theory — strategy frameworks, distinctive-asset science, craft criteria, verification battery, verbal identity.
- `references/inspiration-sources.md`: reference galleries mapped to pipeline stages, GitHub brand-as-code ecosystem (DESIGN.md schema, icon slot canon, DTCG tokens), and AI-era anti-slop practice.

## Guardrails

- Do not derive the brand IP from the skill's own process metaphors or other incidental language; the mark must abstract the product's business scenario and pass the one-sentence buyer test (`references/design-theory.md`).
- Do not accept AI-slop defaults: purple-blue gradient orbs, glassmorphism, sparkle icons, fake 3D depth, default-grotesk typography. Ban them in prompts and reject them in review.
- Do not ship brand color pairings that fail WCAG 2.2 AA contrast; emit palettes as verified foreground/background pairs.
- Do not let rejected exploration files remain in the product-consumable asset tree.
- Do not preserve old brand remotes, names, docs, or assets when the user asks for a complete migration.
- Do not confuse compatibility code named `legacy` with visual legacy assets; inspect context before deleting.
- Do not introduce a landing-page aesthetic into operational software unless the product surface actually calls for it.
- Do not use one-off image outputs as final vectors when the repo needs SVG or platform icon formats.
