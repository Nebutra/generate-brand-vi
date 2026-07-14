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

2. **Strategy tension sheet**
   - State 2-4 business relationships without drawing product nouns.
   - Map each relationship to candidate formal operations.

3. **Parallel operation families**
   - Generate at least three independent black-and-white families.
   - Each family uses one invariant operation across wordmark, symbol, layout and motion.

4. **Collision and neighborhood proof**
   - Test unprompted readings, category similarity and 16-48 px behavior.
   - Reject familiar-object sinks before downstream generation.

5. **Human selection gate**
   - Approve one family or return to the operation branches.
   - No Hero, social, app icon or materialized mark may start before this gate.

6. **Production-clean mark and wordmark**
   - Simplify the seed for legibility and vectorization.
   - Strengthen silhouette and small-size behavior.

7. **App icon variants**
   - Classic, soft/lifestyle, technical/high-contrast, monochrome glyph.
   - Preserve the approved mark; vary only material and environment.

8. **Proof sheets**
   - Small-size legibility, light/dark backgrounds, icon family contact sheet.

9. **Backgrounds and scenes**
   - Hero, social, onboarding, documentation.
   - Use the same approved mark/material references; do not let backgrounds invent new logos.

## Serial Consistency Rules

- Put reference-locking assets before dependent tasks.
- Use image edit/reference inputs for shape consistency when available.
- If using prompt-only generation, explicitly constrain silhouette, composition, forbidden forms, material, lighting, and output intent.
- Promote approved masters to `approved/`; never make downstream tasks depend on exploratory folders.
- Do not use a purely serial mark pipeline before approval; one weak semantic
  decision will contaminate every descendant while appearing visually consistent.

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
