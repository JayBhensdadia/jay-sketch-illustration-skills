---
name: jay-sketch-illustrations
description: Generate Xiaohei-style hand-drawn sketch illustrations for articles. Use when the user asks to generate "sketch", "hand-drawn", "article illustration", "inline illustration", "shot list", or "remove title / edit illustration" for blog posts, Notion docs, workflows, methodology docs, processes, structures, states, metaphors, or ideas. Default style: Xiaohei IP, warm cream paper background, near-black hand-drawn ink, sparse sepia/amber/blue annotations, clean but imaginative. Uses the Paper & Pencil theme palette.
---

# Jay Sketch Illustrations

## Role

Design and generate 16:9 horizontal inline illustrations for articles. The goal is not commercial illustration, PPT infographics, or cute cartoons — it's turning a key judgment, process, structure, state, or metaphor from an article into a clean, absurd, creative, readable-but-not-instructional hand-drawn sketch.

The default visual IP is "Xiaohei" (小黑): a solid-black creature with white dot eyes, thin legs, and a blank expression — seriously doing something absurd but coherent. Xiaohei must be the core action subject, not just decoration.

## References

Load only what the task needs; don't flood context:

- `references/style-dna.md`: Style DNA, colors, theme palette, prohibitions.
- `references/xiaohei-ip.md`: Xiaohei's appearance, personality, action library, and prohibitions.
- `references/composition-patterns.md`: Structure types, original metaphor methods, and no-copy rules.
- `references/prompt-template.md`: Single-image generation prompt template.
- `references/qa-checklist.md`: Post-generation check and iteration rules.
- `assets/examples/`: Low-frequency visual calibration only. Do not include in the default generation path. Do not copy these examples' composition, objects, or labels.

## Workflow

### 1. Digest the article

Read the article, link, Notion page, Markdown file, or screenshot the user provides. Extract:

- What is the core argument
- Which paragraphs carry cognitive turning points
- Which content benefits from visual explanation
- Which parts are better left as text, without illustration

Don't distribute illustrations evenly. Prioritize "cognitive anchors": core judgments, two breakpoints, input-output loops, branching paths, before/after contrasts, one-source-many-uses, handoff paths, common pitfalls, character state changes.

### 2. Output the illustration strategy first

If the user only asks to "analyze where to add illustrations / think about which parts need images", output a shot list first. For each image specify:

- Which paragraph it follows
- The image theme
- The core idea
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested annotation words

Default 4–8 images. 1–3 for short articles; don't exceed 9 even for long articles. Enough is enough — avoid turning the article into a picture book.

### 3. Single image generation

If the user explicitly asks to "generate / output / create / make an image", don't pause for confirmation; use the built-in `image_gen` to generate each image separately. Never combine multiple images into one.

Each image explains only one core structure. The prompt must include:

- 16:9 horizontal article illustration
- Warm cream paper background (#faf7f1, Paper & Pencil theme)
- Near-black hand-drawn line art (#1b1a17)
- Sparse sepia/amber/muted-red/blue handwritten annotations
- Generous empty space
- Xiaohei as the core action subject
- No PPT, no commercial illustration, no cute cartoon, no complex architecture, no title in top-left corner

Don't replicate past examples. Examples only calibrate style density and Xiaohei's participation mode — never directly reuse "conveyor belt breakpoints / Xiaohei pulling the judgment lever / material fish / stamp toolbox / common-pit path" or other known compositions, unless the user explicitly asks to replicate a specific image. Always invent a new strange-but-coherent metaphor from the current article.

### 4. Check and iterate

After generation, check `references/qa-checklist.md`. Regenerate or locally edit if any of the following appear:

- Xiaohei is only decoration
- Scene is too crowded
- Looks like a flowchart / PPT
- Too many annotations or unreadable text
- Top-left corner shows a title like "Common Pitfalls / Flowchart / System Architecture"
- Art style is too cute, childish, or rigid
- Background is not clean cream (#faf7f1)

### 5. Save and deliver

If the user is working in a workspace, copy the final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in order:

```text
01-topic-name.png
02-topic-name.png
```

Preserve the original generated files; don't overwrite existing assets unless the user explicitly asks.

## Output Scope

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- The purpose of each image
- Save paths
- Which images are solid, which are optional

Don't explain style theory at length; let the images speak.
