# Style Explained Daily — Product Image Standard

Use this standard when turning Amazon product photos into catalog assets.

## Output
- Portrait 2:3, 1200 × 1800 pixels, sRGB PNG or optimized WebP.
- Exact flat canvas background: #F8F7F5, including all four corners. No transparent or off-white margins.
- Entire product visible, centered, consistent perceived scale and approximately 10–15% breathing room where practical.
- Natural subtle shadows only. No added typography, watermarks, props, or decorative elements.
- Preserve the actual item: color, texture, construction, hardware, silhouette and proportions. Do not invent features or replace an exact item with a visually similar one.
- When the source is worn by a model, isolate/reconstruct the item carefully; flag any hidden details as uncertain rather than inventing them.

## Mandatory quality control
1. Generate or clean the product cutout.
2. Standardize its canvas with a deterministic image editor; do not rely on an AI prompt to produce exact hex colors or dimensions.
3. Verify output dimensions and sample all four background corners for #F8F7F5.
4. Inspect the full item for altered details, cut-off edges, halos, artificial texture, or incorrect colors.
5. Compare with neighboring product cards at their real website display size.
6. Save to /assets/ and reference the exact filename in data/products.json.

## Website behavior
The website applies a consistent 2:3 product photo area, #F8F7F5 canvas, and object-fit:contain. This avoids cropping and standardizes framing, but CSS cannot remove an existing mismatched background baked into a photo. Older images must be processed and replaced individually or in a batch.
