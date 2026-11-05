# Jay Sketch Illustrations

> Turn the judgments, processes, states, and metaphors inside an article into clean, hand-drawn, absurd inline illustrations — on warm cream notebook paper.
>
> 16:9 horizontal | Xiaohei IP | Warm cream paper (#faf7f1) | Near-black hand-drawn ink | Sparse sepia/amber/blue annotations | Paper & Pencil theme | Codex Skill

---

## What is this?

Jay Sketch Illustrations is a Codex Skill that guides an AI Agent to generate inline illustrations for articles, blog posts, Notion docs, and methodology content.

It is not a general illustration prompt, nor a PPT infographic template. The core goal is: first understand the cognitive anchors in the article, then turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explanatory sketch.

The default visual IP is "Xiaohei" (小黑): a solid-black creature with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, not a corner decoration — Xiaohei is an absurd worker seriously participating in the operation of a system.

The illustration style matches the **Paper & Pencil** site theme: warm cream paper (#faf7f1), near-black ink (#1b1a17), muted sepia/amber accent (#8a5a1f).

In one line: **let AI do more than "add an image" — draw out one key cognitive action from the article.**

---

## Who is this for?

Especially suited for:

- Writers who need inline illustrations and article images
- People making knowledge content, methodology content, or AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want a lighter, stranger, more personally identifiable illustration style than PPT infographics
- People using Codex for content production and wanting a consistent visual language

Not suited for:

- People who want commercial illustration, brand KV, or polished flat illustration
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute IPs, or meme-style images
- People who want to pack long body copy, long explanations, or complete course pages into one image
- People who need strictly editable vector source files

---

## What does it produce?

Default output:

- 16:9 horizontal article illustrations
- A 4–8 image shot list for an article
- For each image: theme, core idea, structure type, Xiaohei's action, and suggested annotation words
- Final PNG files, saved to `assets/<article-slug>-illustrations/` in the workspace

Default non-output:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover KV
- Dense text-heavy infographics

---

## Visual Style

This skill uses the Paper & Pencil theme palette:

- Warm cream paper background (#faf7f1 `--paper`) — not pure white
- Near-black hand-drawn line art (#1b1a17 `--ink`) — fine lines, slight wobble
- Generous empty space — main subject ~40%–60% of canvas
- Sparse sepia/amber (#8a5a1f `--accent`) for primary flow and arrows
- Muted red (#c04848) only for warnings, problems, or key results
- Muted blue (#466480) only for secondary notes or system state
- One image expresses only one core action, structure, state, or metaphor
- Xiaohei must participate in the core action — not decoration
- Absurd, creative, clean — not childish, not commercial

Dark mode variant available: `--paper: #16140f`, `--ink: #ebe4d2`, `--accent: #d6a865`.

---

## Example Illustrations

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-minimum-loop.png)

### One Source, Many Uses

![One Source, Many Uses](examples/images/03-sort-by-purpose.png)

### Handoff Path

![Handoff Path](examples/images/04-one-fish-many-uses.png)

### Information Well

![Information Well](examples/images/10-information-well.png)

### Idea Press

![Idea Press](examples/images/11-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/12-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/14-trust-bridge.png)

These images are style-calibration samples, not composition templates. When using the skill, invent a fresh metaphor from the current article — don't copy these objects or compositions.

---

## Installation

Clone the repo:

```bash
git clone https://github.com/jaybhensdadia/jay-sketch-illustration-skills.git
cd jay-sketch-illustration-skills
```

Copy the skill to your Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installing, use in Codex:

```text
Use $jay-sketch-illustrations to design and generate 5 Xiaohei hand-drawn sketch illustrations for this article.
```

---

## How to use

### Planning only

```text
Use $jay-sketch-illustrations — do not generate images yet.
Analyze the article below and output a shot list of about 5 illustrations.
For each: which paragraph it follows, theme, core idea, structure type, what Xiaohei is doing, suggested annotation words.

<paste article>
```

### Generate inline illustrations directly

```text
Use $jay-sketch-illustrations to generate 4 Xiaohei hand-drawn illustrations for the article below.
Requirements: 16:9 horizontal, warm cream background (#faf7f1), near-black hand-drawn line art, sparse sepia/amber/blue handwritten annotations.

<paste article>
```

### Generate one image for a single concept

```text
Use $jay-sketch-illustrations to generate one article illustration for: "Trust isn't shouted — it's built one piece of evidence at a time."
Scene should be absurd but clean; Xiaohei must carry the core action.
```

### Remove a title or bad text from an image

```text
Use $jay-sketch-illustrations to edit this image: remove the "Flowchart" title in the top-left corner; keep everything else the same.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

1. Read the article, Markdown, Notion content, screenshot, or user-given theme
2. Extract core arguments, cognitive turning points, process structures, and visually suitable paragraphs
3. Output shot list: pick only one cognitive anchor per image
4. For each image, choose a structure type: Workflow, System Detail, Before-After, Character State, Conceptual Metaphor, Method Layers, Map Path, or Comic Strip
5. Invent a new low-tech, absurd-but-coherent physical metaphor
6. Give Xiaohei the core action
7. Generate each image separately using the image model
8. Check against the QA checklist: cream background, white space, Xiaohei's action, annotations, non-PPT feel, no old-example replication
9. Save final PNGs and report purpose and paths

---

## Directory Structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-minimum-loop.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The subdirectory that installs into Codex:

```text
ian-xiaohei-illustrations/
```

The root README, LICENSE, NOTICE, and examples are GitHub documentation.

---

## Notes

- Keep annotation text short — fewer words produce more reliable image generation.
- Each image explains only one core structure; don't turn the article into an instruction manual.
- Xiaohei must carry the core action; if removing Xiaohei leaves the scene fully intact, Xiaohei is too decorative.
- Example images are only for calibrating line density, white space, color restraint, and Xiaohei's vibe — don't copy compositions.
- Image models can produce spelling errors, hallucinated labels, style drift, or unwanted titles — always check after generation.
- If annotation text is badly wrong, reduce the number of labels and regenerate.

---

## License

MIT License. See [LICENSE](LICENSE).
