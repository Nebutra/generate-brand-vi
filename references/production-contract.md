# Brand VI Production Contract

Use this contract whenever the user asks to produce, deliver, build, complete or
generate a brand VI. Exploration requests are different and may stop at studies.

## Definition of done

A production request is not complete when image generation succeeds. It is
complete only when every selected deliverable is one of:

- `complete`: source, export and acceptance evidence exist;
- `blocked`: a named gate, missing input and resume action are recorded;
- `not-applicable`: intentionally excluded with rationale;
- `external-handoff`: concept/specification and supplier acceptance criteria exist.

Never report a small exploratory batch as the delivered VI.

## Execution model

1. Compile selected modules into `brand-vi-production-plan.json`.
2. Produce strategy and foundations first.
3. Run mark families in parallel and stop only the mark-dependent branch at
   `mark-approved`.
4. Continue all independent product, language, token, accessibility, trust and
   governance deliverables while the mark is under review.
5. Resume dependent applications after mark approval without rebuilding
   completed independent work.
6. Finish with an item-level status and acceptance report.

## Gate semantics

- A gate blocks only tasks that declare that gate.
- A rejected mark does not end a production run.
- Missing physical measurements block only affected packaging, vehicle,
  apparel, retail, environment or wayfinding deliverables.
- Missing legal evidence blocks claims and approvals, not neutral templates or
  evidence-request checklists.

## Producer semantics

`generate-image` is one producer for raster exploration and imagery. It is not
the Brand VI production engine. Use structured documents, SVG/vector editing,
design tokens, HTML/CSS, office-document tools, motion/audio workflows and
specialist handoffs according to each plan item's `producer` and `output`.
