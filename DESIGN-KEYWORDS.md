# 22 Background Design Keywords

A ready-to-use reference for making flat AI-generated backgrounds less flat: append one of these
keywords to a base prompt. Recorded by hand from Charles Liu's video
"22 Backgrounds to Make Designs Less Flat (in under 30 seconds)" (Douyin), screenshot verified
2026-11-25.

These are not links to skill repos — they're a vocabulary list for prompt-writing, kept here so it
sits next to the design skills it's used with (see [`STACKS.md`](STACKS.md) for the design stack).

## The 22 at a glance

One render per keyword, made with the sample prompt under its name below.

![All 22 background styles at a glance](assets/backgrounds/00-all-22-overview.webp)

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

## Sample prompts, one per style

Full prompts, not fragments: each one is ready to paste into an image model as a website hero or
section background. Under each name sits one render of its prompt (1280×853 WebP, kept in
`assets/backgrounds/`), so you can see the style before you paste anything. Swap four things to make any of them yours — the **palette**, the **aspect
ratio**, the **side the text sits on**, and the **subject** if you want something in the frame.
The rest (lighting, negative space, "no text") is what keeps them usable as backgrounds.

Every prompt ends with a no-text instruction (`no text, no lettering`, or a stricter variant for the
styles that attract numbers and words). Keep that even when you do want a title: render it
in the layout, not the image, or the model will invent lettering you cannot edit.

### Texture and material

**1. Felt texture**

![Example render: felt texture](assets/backgrounds/01-felt-texture.webp)

> Website hero background, soft felt fabric texture filling the frame, fuzzy woven fibre surface in deep navy with a faint warm light falling from the top left, gentle fibre shadow for depth, calm empty space across the upper third, shot flat-on, even diffused studio light, 16:9, no text, no lettering, no logos.

**2. Fluted glass**

![Example render: fluted glass](assets/backgrounds/02-fluted-glass.webp)

> Website hero background, fluted reeded glass panel filling the frame, ribbed translucent surface refracting a teal and amber gradient behind it, soft vertical highlights along each rib, shallow depth of field, calm negative space on the left for a headline, studio lighting, 16:9, no text, no lettering.

**5. Speckled graphite**

![Example render: speckled graphite](assets/backgrounds/05-speckled-graphite.webp)

> Website hero background, dark speckled graphite stone surface, fine grey mineral flecks on a near-black ground, matte finish, subtle raking light from the right, deep uncluttered space across the middle for white type, 16:9, no text, no lettering.

**10. Grass texture**

![Example render: grass texture](assets/backgrounds/10-grass-texture.webp)

> Website hero background, close-up macro grass texture, individual blades catching low morning light, shallow depth of field, dark green and muted gold palette, empty darker area top-left for a headline, 16:9, no text, no lettering.

**12. Paper texture**

![Example render: paper texture](assets/backgrounds/12-paper-texture.webp)

> Website hero background, uncoated recycled paper texture, visible fibre grain and a faint deckled edge shadow, warm off-white ground, soft window light from the side, generous margins for type, 16:9, no text, no lettering.

### Gradient and colour field

**3. Thermal gradients**

![Example render: thermal gradients](assets/backgrounds/03-thermal-gradients.webp)

> Website hero background, abstract thermal heatmap gradient, deep blue through magenta into amber, smooth organic contour transitions, slight grain, darkened corners so light text stays legible, 16:9, no text, no lettering.

**9. Grainy gradients**

![Example render: grainy gradients](assets/backgrounds/09-grainy-gradients.webp)

> Website hero background, grainy gradient colour wash from deep navy to teal, visible film grain, smooth falloff with no banding, subtle vignette, 16:9, no text, no lettering.

**17. Stippled gradients**

![Example render: stippled gradients](assets/backgrounds/17-stippled-gradients.webp)

> Website hero background, stippled gradient drawn as a field of crisp round ink dots all the same size, amber dots densely packed on the left and thinning evenly to sparse on the right, on flat charcoal paper, clean vector-like stipple shading, smooth dot-screen gradient, large calm area for a headline on the right, 16:9, no text, no lettering.

**19. Blurred photos**

![Example render: blurred photos](assets/backgrounds/19-blurred-photos.webp)

> Website hero background, heavily blurred photograph, soft bokeh field of teal and amber light, no discernible subject, darker upper half for white type, cinematic, 16:9, no text, no lettering.

**20. Iridescent shapes**

![Example render: iridescent shapes](assets/backgrounds/20-iridescent-shapes.webp)

> Website hero background, iridescent holographic shapes floating on a near-black field, oil-slick rainbow reflections along the edges, soft rim light, dark open negative space on the left, 16:9, no text, no lettering.

### Technical and diagrammatic

**7. Blueprint grids**

![Example render: blueprint grids](assets/backgrounds/07-blueprint-grids.webp)

> Website hero background, blueprint drafting grid, fine cyan lines on deep navy paper, faint technical construction marks toward the edges, clear unmarked centre, subtle paper tooth, 16:9, no readable text, no numbers, no lettering.

**13. Contour lines**

![Example render: contour lines](assets/backgrounds/13-contour-lines.webp)

> Website hero background, topographic contour line map, thin elevation lines in muted teal over deep navy, lines thinning and fading toward the top for a headline, subtle glow at two peaks, 16:9, no text, no numbers, no lettering.

**18. Square-dot grids**

![Example render: square-dot grids](assets/backgrounds/18-square-dot-grids.webp)

> Website hero background, square dot grid, evenly spaced small square dots on a warm light grey field, one denser band sweeping across the middle, minimal, 16:9, no text, no lettering.

### Print and retro

**8. Halftone**

![Example render: halftone](assets/backgrounds/08-halftone.webp)

> Website hero background, halftone dot pattern, large soft dots fading from dense to sparse across the frame, duotone amber on near-black, gentle rotation for movement, 16:9, no text, no lettering.

**11. Dithered images**

![Example render: dithered images](assets/backgrounds/11-dithered-images.webp)

> Website hero background, 1-bit ordered dither pattern, retro dithered texture dissolving into smooth dark space at the top, black and pale amber, crisp pixels, 16:9, no text, no lettering.

**15. Pixel mosaics**

![Example render: pixel mosaics](assets/backgrounds/15-pixel-mosaics.webp)

> Website hero background, pixel mosaic of large blocky tiles in a restrained four-colour palette, grid dissolving toward the edges, flat and graphic, clean centre, 16:9, no text, no lettering.

**22. ASCII and pixels**

![Example render: ASCII and pixels](assets/backgrounds/22-ascii-and-pixels.webp)

> Website hero background, ASCII art character field, dense monospace glyphs in pale green on near-black, pattern thinning into dark space across the top for a headline, crisp terminal aesthetic, 16:9, no readable words, no lettering.

### Photo and capture

**4. Water ripples**

![Example render: water ripples](assets/backgrounds/04-water-ripples.webp)

> Website hero background, caustic water ripples, sunlight refracting through a shallow pool onto pale concrete, shifting teal light patterns, calm area top-centre for type, 16:9, no text, no lettering.

**6. Single-hue landscapes**

![Example render: single-hue landscapes](assets/backgrounds/06-single-hue-landscapes.webp)

> Website hero background, monochrome single-hue landscape, layered blue hills fading into haze, minimal and quiet, open sky filling the upper half for a headline, soft fog, 16:9, no text, no lettering.

**14. Cloud sky**

![Example render: cloud sky](assets/backgrounds/14-cloud-sky.webp)

> Website hero background, soft cloud sky at dusk, gentle gradient from violet to peach, wispy high cloud, open sky across the upper two thirds, 16:9, no text, no lettering.

**16. Lens distortion**

![Example render: lens distortion](assets/backgrounds/16-lens-distortion.webp)

> Website hero background, abstract colour field warped by strong barrel lens distortion, chromatic fringing at the frame edges, deep navy and teal, clean undistorted centre, 16:9, no text, no lettering.

### Fine art

**21. Impressionist paintings**

![Example render: impressionist paintings](assets/backgrounds/21-impressionist-paintings.webp)

> Website hero background, impressionist painting surface, visible oil brushstrokes in muted blue and warm ochre, soft focus, painterly canvas texture, calm area for a headline, 16:9, no text, no lettering.

### Using these on a real site

- Generators give you one aspect ratio per call, so ask for **16:9** and crop to your hero ratio
  afterwards rather than trusting the model to letterbox. Export **WebP at 1536×960 or 1600×900**,
  under about 200 KB, and ship a separate smaller file for mobile.
- A background carrying a headline needs contrast at the text area, not overall prettiness. If the
  render comes back busy exactly where the title goes, add "darkened left third" or "vignette" to
  the prompt instead of lowering opacity in CSS later.
- Keep one style across a site, not one per page. If you need variety, vary the palette inside the
  same keyword rather than switching keywords.
- To build the site that goes around the background, start from the
  [`website-starter` skill](authored/website-starter/SKILL.md): a fill-in prompt plus the launch checklist.

## Avoid pairing

- Two print/retro keywords at once (halftone + dither) reads as noise, not texture
- ASCII/pixel keywords with a photo subject, the glyph noise eats the silhouette
- Iridescent + thermal gradients together, both are high-saturation and fight
