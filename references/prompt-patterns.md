# Prompt Patterns

## Foundation Board Prompt

Use for mood, palette, and material before logo work:

```text
Create a <brand> material and palette reference board, not a logo.
Arrange <materials/metaphors> in a clean <layout style>.
Palette: <named colors>. Lighting: <direction/quality>.
Design feeling: <era/product/culture>. No text, no logo, no watermark.
```

## Form-Family Study Prompt

```text
Create a black-and-white identity study for <brand>, not a finished logo.
Business tension: <force A> versus/with <force B>.
Explore one formal operation only: <split/join/offset/phase/fold/repeat/shared-axis/etc>.
Apply it consistently to one wordmark fragment, one monogram or symbol, one
layout motif, and one motion keyframe sequence. Show construction relationships,
not materials or mockups. Avoid literal pictograms and these semantic
collisions: <specific nouns/category clichés>. No gradients, effects or generated prose.
```

Run this prompt separately for at least three operations. Do not ask one
generation to produce a random logo grid; each family needs a stated invariant.

## Approved Direction Prompt

```text
Refine the approved <brand> form family governed by <operation>.
Preserve these invariants: <geometry/spacing/relationship>.
Remove incidental object readings identified in review: <collisions>.
Produce a black-and-white primary mark and wordmark relationship at 16, 24,
32 and 48 px. No material, mockup, gradient, lighting or extra symbol.
```

## Production Icon Prompt

```text
Convert the approved <brand> mark into a production app icon asset.
Preserve the exact mark relationship: <shape + signal>.
Target: <desktop/mobile/web>. Output intent: <transparent/opaque/adaptive>.
Use <material/lighting/depth>. Readable at 48 px.
Do not add <extra stones/background/tile/text/old brand>.
```

## Background Prompt

```text
Create a <brand> <hero/social/onboarding> background using the approved mark and material references.
Composition: <where product screenshot/text will sit>.
Mood: <culture/product tone>. Keep low visual noise behind UI.
No generated text, no extra logos, no watermark.
```

## Standing Negative Constraints (append to every generation prompt)

Ban the AI-slop signature explicitly; models default to it:

```text
No purple-blue gradients, no floating gradient orbs, no glassmorphism,
no sparkle/star AI icons, no fake 3D depth or bevels, no watermark,
no generated text.
```

## Prompt Hygiene

- Name colors and materials; do not rely on vague “modern” alone.
- State product context: developer tool, consumer app, operational SaaS, game, venue, etc.
- State what must stay fixed and what may vary.
- Use “not a logo” for foundation boards to prevent premature marks.
- Use “approved mark” for downstream outputs to prevent drift.
- Never include a concrete object metaphor unless the brand is intentionally
  pictorial and collision review has approved that object.
- Prefer verbs and spatial relationships over nouns: interrupt, align, retain,
  reverse, attenuate, branch, rejoin, offset, phase and contain.
