# QA Checklist

## Must Pass

- Is 16:9 horizontal.
- Background is clean warm cream (#faf7f1).
- Xiaohei is present.
- Xiaohei performs the core action, not just decoration.
- Did not replicate an old example composition — invented a fresh metaphor for the current article.
- Scene is absurd, creative, interesting.
- Clean and airy; main subject doesn't exceed roughly 60% of the canvas.
- One image explains only one core structure.
- Annotations are sparse, short, readable.
- Sepia/amber (#8a5a1f) used only for primary path or arrows.
- Muted red (#c04848) used only for key points, problems, warnings, or results.
- Muted blue (#466480) used only for supplementary notes, feedback, or system state.

## Failure Signals

Regenerate or locally edit if any of the following appear:

- Top-left corner has a title: "Common Pitfalls / Workflow / System Architecture / Roadmap".
- Xiaohei looks like a mascot, emoji, or cute cartoon.
- Scene looks like a PPT, course slide, or formal flowchart.
- Too many elements, too many arrows, too many nodes.
- Text becomes a long paragraph explanation.
- Background has paper texture, shadows, gradients, beige or warm-gray tints that look designed rather than natural cream, noise.
- Real UI screenshots or tech-interface feel.
- Annotations are unreadable or badly misspelled.
- Scene is too rigid, no absurd metaphor.
- Too similar in composition to any image in `assets/examples/`.

## Iteration Methods

- Too generic: make Xiaohei the action subject; add one strange-but-coherent metaphor.
- Too complex: remove nodes; keep only one action and 3–5 short annotations.
- Too cute: emphasize deadpan, blank serious expression, not cute, not mascot.
- Too PPT: remove titles, borders, tidy grids, and excess arrows; shift to a hand-drawn scene.
- Too similar to old examples: keep the core idea; swap out the main object and Xiaohei's action.
- Text errors: prefer local editing; if errors are widespread, regenerate and reduce annotation count.

## Delivery Standard

A high-quality image should make the reader think "that's a bit strange" first, then understand the structure within one second.

If the first impression is "tutorial page" rather than "absurd product sketch on cream notebook paper", it doesn't pass.
