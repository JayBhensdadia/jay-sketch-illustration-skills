# Image Generation Prompt Template

Generate each image separately. Replace the variables below based on the article content. Never combine multiple images into one.

```text
Generate one standalone 16:9 horizontal article illustration.

Visual DNA:
Warm cream paper background (#faf7f1 — Paper & Pencil theme). Minimalist near-black (#1b1a17) hand-drawn line art. Slightly wobbly pen lines. Lots of empty cream space. Sparse handwritten annotations in muted sepia/amber (#8a5a1f), muted red (#c04848), and muted blue (#466480). Clean absurd product-sketch feeling on a ruled notebook page. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
Xiaohei (小黑), a small solid-black absurd creature with white dot eyes, tiny thin legs, blank serious expression, slightly uneven hand-drawn body shape. Xiaohei must perform the core conceptual action, not decorate the scene. Make Xiaohei serious, deadpan, and slightly bizarre, not cute.

Theme:
{illustration theme}

Structure type:
{Workflow / System Detail / Before-After / Character State / Conceptual Metaphor / Method Layers / Map Path / Comic Strip}

Core idea:
{the single core idea this image must convey}

Composition:
{specific scene: where Xiaohei is, what Xiaohei is doing, what the main objects are, how information flows}

Suggested elements:
{element 1} / {element 2} / {element 3} / {element 4}

Handwritten labels:
{label 1} / {label 2} / {label 3} / {label 4} / {optional label 5}

Color use:
Near-black (#1b1a17) for main line art and Xiaohei. Sepia/amber (#8a5a1f) for main flow/path/arrows. Muted red (#c04848) only for key warnings/problems/results. Muted blue (#466480) only for secondary notes or system/feedback state. Background: warm cream (#faf7f1).

Constraints:
One image explains only one core structure. Keep the main subject around 40%–60% of the canvas. Preserve at least 35% open cream space. Use at most 5–8 short handwritten labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## Edit prompts

Remove a top-left title:

```text
Edit the provided image. Remove only the handwritten title "{text to remove}" and its underline from the top-left corner. Fill that area with the same warm cream background (#faf7f1), matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

Strengthen Xiaohei's role:

```text
Regenerate this illustration with the same core meaning and simple layout, but make Xiaohei more central to the conceptual action. Xiaohei should be doing the strange work that explains the idea, not standing beside the diagram. Keep it clean, sparse, hand-drawn, and not cute. Maintain the warm cream paper background (#faf7f1) and near-black ink (#1b1a17).
```

Dark mode variant:

```text
Regenerate this illustration for a dark-theme notebook page. Change the background to very dark warm paper (#16140f), line art to warm light ink (#ebe4d2), and primary flow color to warm amber (#d6a865). Keep the same composition, structure, Xiaohei, and labels. Everything else stays the same.
```
