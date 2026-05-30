---
name: doctor-beagle-illustrations
description: Generate clean, absurd, hand-drawn article illustrations for Traditional Chinese or English writing. Use when the user asks for body illustrations, article visuals, visual metaphors, shot lists, image prompts, or image edits for essays, blogs, Notion docs, workflows, methods, concepts, and structure/state explanations. Default recurring character is the Doctor Beagle visual IP, using pure white backgrounds, sparse black line art, tan beagle markings, restrained red/orange/blue handwritten notes, and image_gen with bundled beagle reference sheets.
---

# Doctor Beagle Illustrations

## Core

Design and generate 16:9 horizontal article illustrations for Traditional Chinese or English content.

The goal is not commercial illustration, PPT infographics, cute pet stickers, or polished mascot posters. Turn an article's key judgement, workflow, structure, state, or metaphor into one clean, strange, readable hand-drawn explanation image.

Default recurring IP is **Doctor Beagle**: a compact short-legged beagle with floppy tan ears, tiny black dot eyes, black oval nose, white muzzle and belly, tan/brown patches, and a serious deadpan working attitude. Doctor Beagle must participate in the core conceptual action, not stand beside the image as decoration.

## Language Rules

- Use **Traditional Chinese** by default for user-facing strategy, labels, and generated Chinese handwriting.
- Use **English** when the source article or user request is English.
- Do not use Simplified Chinese unless the user explicitly asks for it or the source text requires verbatim Simplified Chinese.
- Keep in-image labels short: usually 2-8 characters for Chinese, 1-4 words for English.

## References

Load only what the current task needs:

- `references/style-dna.md`: visual DNA, color rules, writing rules, hard bans.
- `references/doctor-beagle-ip.md`: Doctor Beagle proportions, markings, behavior, action vocabulary, failure cases.
- `references/composition-patterns.md`: structure types, metaphor generation, repeat-avoidance rules.
- `references/prompt-template.md`: single-image `image_gen` prompt template and edit prompts.
- `references/qa-checklist.md`: post-generation QA and iteration rules.
- `references/beagle-visual-anchors.md`: how to use the bundled character sheets.
- `assets/reference/`: visual anchors for character consistency. Use them as image references before first generation when character fidelity matters.

## Workflow

### 1. Understand the Source

Read the user's article, Markdown, Notion content, screenshot, notes, or concept. Extract:

- the core judgement
- the cognitive turning points
- the process, structure, or state worth visualizing
- the parts that should remain text-only

Do not illustrate evenly. Prefer cognitive anchors: a core claim, breakpoint, input/output loop, routing split, before/after contrast, reuse of one source, handoff path, common pitfall, or role/state transition.

### 2. Produce a Shot List When Asked

If the user asks to plan illustrations, analyze where to add images, or says not to generate images yet, output a concise shot list.

For each proposed image include:

- where it goes in the article
- theme
- core idea
- structure type
- what Doctor Beagle is doing
- suggested elements
- suggested short labels

Default to 4-8 images. For a short article, use 1-3. For a long article, do not exceed 9 unless the user asks for a larger set.

### 3. Generate with `image_gen`

When the user explicitly asks to generate, output, draw, create images, or edit an image, do not stop for confirmation unless required details are missing. Use the built-in `image_gen` tool. Generate each image separately. Never combine multiple article illustrations into one sheet unless the user asks for a sheet.

Before the first Doctor Beagle generation in a task, use the bundled visual anchors when character consistency matters:

- `assets/reference/beagle-model-sheet.png` for proportions and views
- `assets/reference/beagle-action-poses.png` for action vocabulary
- `assets/reference/beagle-detail-sheet.png` for head shape, ears, markings, and palette

Each generation prompt must include:

- 16:9 horizontal article illustration
- pure white background
- minimalist black hand-drawn line art
- Doctor Beagle as the core action subject
- compact short-legged beagle, floppy tan ears, black dot eyes, black oval nose, white muzzle/belly, tan patches
- sparse red/orange/blue handwritten notes
- lots of empty white space
- no PPT, no commercial illustration, no childlike cute poster, no dense architecture, no top-left type title

Do not copy old examples or previous generated compositions. Re-invent a fresh low-tech visual metaphor for the current article.

### 4. Check and Iterate

After generation, use `references/qa-checklist.md`. Regenerate or edit when:

- Doctor Beagle is only decorative
- the character drifts away from the reference sheets
- the image is too full
- it looks like a flowchart, slide, or formal diagram
- there is too much text or obvious text corruption
- a top-left title appears, such as "workflow", "system map", or "common pitfalls"
- the style becomes childish, mascot-like, commercial, realistic, or rigid
- the background is not clean white

### 5. Save Deliverables

If the user is working in a workspace, copy final images to:

```text
assets/<article-slug>-illustrations/
```

Use ordered filenames:

```text
01-topic-name.png
02-topic-name.png
```

Keep original generated files. Do not overwrite existing assets unless the user explicitly asks for replacement.

## Response Style

Before generation, keep strategy short and specific. After generation, report:

- how many images were generated
- each image's use
- saved paths
- which images are strongest and which are optional

Do not write long style theory. Let the images do the work.
