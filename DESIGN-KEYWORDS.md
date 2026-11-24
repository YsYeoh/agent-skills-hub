# 22 Background Design Keywords

A ready-to-use reference for making flat AI-generated backgrounds less flat: append one of these
keywords to a base prompt. Recorded by hand from Charles Liu's video
"22 Backgrounds to Make Designs Less Flat (in under 30 seconds)" (Douyin), screenshot verified
2026-11-25.

These are not links to skill repos — they're a vocabulary list for prompt-writing, kept here so it
sits next to the design skills it's used with (see [`STACKS.md`](STACKS.md) for the design stack).

## The 22

| #  | Keyword                | Category    | AI-ready prompt fragment |
|----|------------------------|-------------|--------------------------|
| 1  | Felt texture           | Texture     | soft felt fabric texture background, fuzzy woven surface |
| 2  | Fluted glass           | Material    | fluted reeded glass panel background, ribbed translucent glass |
| 3  | Thermal gradients      | Gradient    | thermal camera heatmap gradient background, orange-to-blue IR gradient |
| 4  | Water ripples          | Nature      | caustic water ripple background, sunlight refraction on pool surface |
| 5  | Speckled graphite      | Texture     | speckled graphite stone background, dark grey mineral flecks |
| 6  | Single-hue landscapes  | Photography | monochrome single-hue landscape background, tonal blue hills |
| 7  | Blueprint grids        | Technical   | blueprint grid background, cyan technical drafting lines |
| 8  | Halftone               | Print       | halftone dot pattern background, vintage CMYK screen print |
| 9  | Grainy gradients       | Gradient    | grainy noisy gradient background, film grain colour wash |
| 10 | Grass texture          | Nature      | close-up grass texture background, macro lawn blades |
| 11 | Dithered images        | Retro       | dithered pixel image background, 1-bit ordered dither retro art |
| 12 | Paper texture          | Texture     | textured paper background, uncoated recycled paper grain |
| 13 | Contour lines          | Technical   | topographic contour line background, elevation map lines |
| 14 | Cloud sky              | Nature      | soft cloud sky background, pastel atmosphere backdrop |
| 15 | Pixel mosaics          | Retro       | pixel mosaic background, blocky low-res tile art |
| 16 | Lens distortion        | Photo fx    | lens distortion background, barrel warp chromatic edge blur |
| 17 | Stippled gradients     | Illustration| stippled dot gradient background, pointillism shading |
| 18 | Square-dot grids       | Technical   | square dot grid background, dotted matrix paper |
| 19 | Blurred photos         | Photo fx    | heavily blurred photo background, soft bokeh colour field |
| 20 | Iridescent shapes      | Abstract    | iridescent holographic shape background, oil-slick rainbow forms |
| 21 | Impressionist paintings| Art         | impressionist painting background, visible brushstroke colour field |
| 22 | ASCII and pixels       | Retro       | ASCII art character background, monospace terminal glyphs |

## Grouped by what they are

- **Texture / material**: felt (1), speckled graphite (5), grass (10), paper (12)
- **Gradient / colour field**: thermal (3), grainy (9), stippled (17), blurred photos (19), iridescent (20)
- **Technical / diagrammatic**: blueprint grids (7), contour lines (13), square-dot grids (18)
- **Print / retro**: halftone (8), dithered (11), pixel mosaics (15), ASCII and pixels (22)
- **Photo / capture**: water ripples (4), single-hue landscapes (6), cloud sky (14), lens distortion (16)
- **Fine art**: impressionist paintings (21)
- **Glass / synthetic**: fluted glass (2)

## How to use them

Append one keyword to a base prompt, for example:

> "minimal tech blog cover background, <KEYWORD>, deep navy base with teal and amber accent glow,
> generous negative space in the upper third for a title, flat vector illustration, no text"

Order matters for legibility: put the background keyword **after** the subject, and repeat
"no text, no lettering" when the subject carries a title — gradient and ASCII keywords tend to pull
legible-looking glyph noise into the render.

## Avoid pairing

- Two print/retro keywords at once (halftone + dither) reads as noise, not texture
- ASCII/pixel keywords with a photo subject, the glyph noise eats the silhouette
- Iridescent + thermal gradients together, both are high-saturation and fight
