# Prompt Template

Use `image_gen` for generation. Generate each image separately. Replace the placeholders with article-specific details.

Before the first generation in a task, inspect or attach the relevant visual anchors when character fidelity matters:

- `assets/reference/beagle-model-sheet.png`
- `assets/reference/beagle-action-poses.png`
- `assets/reference/beagle-detail-sheet.png`

```text
Generate one standalone 16:9 horizontal article illustration.

Language:
Use Traditional Chinese handwritten labels unless the user asks for English or the source article is English. Do not use Simplified Chinese.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse red/orange/blue handwritten notes. Clean absurd product-sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
Doctor Beagle, a compact short-legged beagle with large rounded floppy tan ears, tiny black dot eyes, black oval nose, white muzzle and belly, tan/brown head patches and side patch, small tail, deadpan serious expression, slightly uneven hand-drawn outline. Doctor Beagle must perform the core conceptual action, not decorate the scene. Keep the character consistent with the bundled beagle reference sheets.

Theme:
{article illustration theme}

Structure type:
{Workflow / System Fragment / Before-After Contrast / Character State / Concept Metaphor / Method Layers / Map or Route / Mini Comic}

Core idea:
{the single idea this image should express}

Composition:
{where Doctor Beagle is, what it is doing, main object, how information or action flows}

Suggested elements:
{element 1} / {element 2} / {element 3} / {element 4}

Handwritten labels:
{label 1} / {label 2} / {label 3} / {label 4} / {optional label 5}

Color use:
Black for main line art, objects, and primary notes. Tan/brown only for Doctor Beagle markings. Orange only for main flow/path/thread/arrow. Red only for key warnings/problems/results. Blue only for secondary notes or system state.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not generate the old Xiaohei black creature. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## Edit Prompt: Remove a Bad Title

```text
Edit the provided image. Remove only the handwritten title "{text to remove}" and its underline from the top-left corner. Fill that area with the same clean white background. Preserve everything else exactly: Doctor Beagle, labels, paths, line style, composition, aspect ratio, and image quality. Do not add new text or objects.
```

## Regeneration Prompt: Improve Beagle Participation

```text
Regenerate this illustration with the same core meaning and simple layout, but make Doctor Beagle perform the central conceptual action. Doctor Beagle should do the strange work that explains the idea, not stand beside the diagram. Keep it pure white, sparse, hand-drawn, deadpan, and consistent with the reference sheets.
```

## Regeneration Prompt: Fix Character Drift

```text
Regenerate with stronger Doctor Beagle consistency. Match the bundled beagle reference sheets: compact short-legged body, floppy tan ears, tiny black dot eyes, black oval nose, white muzzle and belly, tan/brown patches, small tail, deadpan serious expression, simple hand-drawn black line. Do not make it realistic, plush, anime, sticker-like, or childlike.
```

