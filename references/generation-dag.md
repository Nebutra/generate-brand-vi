# Generation DAG Patterns

## Built-in Backend

Run brand DAGs through the bundled adapter:

```bash
python3 scripts/run_brand_image_dag.py --repo /path/to/project
python3 scripts/run_brand_image_dag.py --repo /path/to/project --execute
```

The first command is a free dry-run. The second makes billed calls after approval.
The adapter discovers a sibling or globally installed `generate-image`, defaults to
`mox`, and lets that backend resolve the global `MOX_API_KEY`. Override discovery
with `GENERATE_IMAGE_SKILL=/path/to/generate-image`; never pass the key on the
command line.

## Recommended DAG

1. **Foundation material board**
   - Palette, material, lighting, texture, cultural mood.
   - No logo or text.

2. **Symbol motif sheet**
   - Small visual metaphors derived from the philosophy.
   - Establish shape vocabulary and negative constraints.

3. **Core mark seed**
   - One primary logo direction.
   - Use foundation/motif references when consistency is needed.

4. **Production-clean mark**
   - Simplify the seed for legibility and vectorization.
   - Strengthen silhouette and small-size behavior.

5. **App icon variants**
   - Classic, soft/lifestyle, technical/high-contrast, monochrome glyph.
   - Preserve the approved mark; vary only material and environment.

6. **Proof sheets**
   - Small-size legibility, light/dark backgrounds, icon family contact sheet.

7. **Backgrounds and scenes**
   - Hero, social, onboarding, documentation.
   - Use the same approved mark/material references; do not let backgrounds invent new logos.

## Serial Consistency Rules

- Put reference-locking assets before dependent tasks.
- Use image edit/reference inputs for shape consistency when available.
- If using prompt-only generation, explicitly constrain silhouette, composition, forbidden forms, material, lighting, and output intent.
- Promote approved masters to `approved/`; never make downstream tasks depend on exploratory folders.

## Negative Constraints

Write negative constraints as visual risks, not just “ugly”:

- no old brand mark;
- no body-part/anatomical silhouette;
- no misleading letterform;
- no mascot if the product is not mascot-led;
- no fake generated text;
- no watermark;
- no decorative tile if the target platform supplies the mask/background.

## Cleanup

After approval, delete or move rejected generations outside the product repo. A future agent will treat files in `resources/brand/generated/` as usable unless the directory structure says otherwise.
