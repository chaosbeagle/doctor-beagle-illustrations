# Beagle Visual Anchors

Use these images to reduce character drift when generating with `image_gen`.

## Assets

- `assets/reference/beagle-model-sheet.png`
  - Use for body proportions, front/side/rear views, short legs, floppy ears, compact silhouette.
- `assets/reference/beagle-action-poses.png`
  - Use for typical conceptual work actions: pulling, carrying, pushing, sniffing, sitting, tagging, tugging, lying flat.
- `assets/reference/beagle-detail-sheet.png`
  - Use for head shape, white muzzle, tan ear shape, patch placement, eye/nose style, and palette.

## When to Load

Load or inspect the anchors before the first generation in a task when:

- the user asks for final images, not just a shot list
- the image must keep Doctor Beagle consistent across multiple outputs
- a previous output drifted into a generic dog, puppy mascot, realistic beagle, or old Xiaohei-style figure

For a single quick draft, `beagle-model-sheet.png` is usually enough.

For a multi-image set, use all three anchors.

## Prompt Clause

Add this clause to generation prompts when using the anchors:

```text
Match the provided Doctor Beagle reference sheets for character consistency: compact short-legged beagle, large rounded floppy tan ears, tiny black dot eyes, black oval nose, white muzzle and belly, tan/brown head and side patches, small tail, deadpan serious expression, simple wobbly black line art. Use the references for the character only; invent a new article-specific metaphor and composition.
```

## Do Not

- Do not copy the model sheet layout into article illustrations.
- Do not reuse action-sheet poses literally unless they fit the article.
- Do not add labels from the reference sheets into final images.
- Do not let the anchors override the article's core metaphor.

