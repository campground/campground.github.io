---
name: Campground
description: Digital agency and consultancy site, built on the Campground Design System.
colors:
  pine: "#006636"
  pine-hover: "#00522a"
  pine-tint: "#dff3e4"
  pine-wash: "#f0faf3"
  moss: "#417703"
  moss-inverse: "#81bc55"
  dusk: "#332d70"
  dusk-hover: "#28215f"
  dusk-label: "#745ca5"
  dusk-pale: "#d5d7fc"
  dusk-tint: "#eaebfe"
  dusk-wash: "#f5f6ff"
  lantern: "#a1a2ec"
  lantern-bright: "#caccff"
  ember: "#ff8a80"
  night-ground: "#131520"
  night-raised: "#1b1e28"
  night-line: "#393d48"
  night-muted: "#bbbdc6"
  night-ink: "#ebeef7"
  granite: "#3d3f44"
  granite-muted: "#5c5f66"
  birch: "#f6f7f4"
  birch-sunken: "#eceee9"
  white: "#ffffff"
  line: "#d9dcd5"
  line-strong: "#7d8186"
  danger: "#a8261d"
  danger-tint: "#fbe9e7"
typography:
  display:
    fontFamily: "Arvo, Rockwell, Georgia, serif"
    fontSize: "56px"
    fontWeight: 400
    lineHeight: "60px"
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "Arvo, Rockwell, Georgia, serif"
    fontSize: "40px"
    fontWeight: 400
    lineHeight: "46px"
    letterSpacing: "-0.01em"
  title:
    fontFamily: "Arvo, Rockwell, Georgia, serif"
    fontSize: "22px"
    fontWeight: 700
    lineHeight: "28px"
  body-lg:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: "28px"
  body:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: "24px"
  body-sm:
    fontFamily: "Archivo, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: "20px"
  label-lg:
    fontFamily: "Archivo Expanded, Archivo, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 700
    lineHeight: "20px"
    letterSpacing: "0.12em"
  label:
    fontFamily: "Archivo Expanded, Archivo, system-ui, sans-serif"
    fontSize: "12px"
    fontWeight: 700
    lineHeight: "16px"
    letterSpacing: "0.12em"
rounded:
  xs: "2px"
  sm: "4px"
spacing:
  row: "16px"
  panel-y: "20px"
  gutter: "24px"
  panel: "24px"
  panel-lg: "32px"
  column-gap: "48px"
  step-gap: "48px"
  footer: "64px"
  section: "96px"
  section-lg: "128px"
components:
  button-primary:
    backgroundColor: "{colors.pine}"
    textColor: "{colors.white}"
    typography: "{typography.label}"
    rounded: "{rounded.xs}"
    padding: "0 24px"
    height: "44px"
  button-primary-hover:
    backgroundColor: "{colors.pine-hover}"
  button-hero:
    backgroundColor: "{colors.pine}"
    textColor: "{colors.white}"
    rounded: "{rounded.xs}"
    padding: "0 32px"
    height: "54px"
  button-nav:
    backgroundColor: "{colors.pine}"
    textColor: "{colors.white}"
    typography: "{typography.label}"
    rounded: "{rounded.xs}"
    padding: "0 24px"
    height: "48px"
  button-inverse:
    backgroundColor: "{colors.white}"
    textColor: "{colors.dusk}"
    typography: "{typography.label}"
    rounded: "{rounded.xs}"
    padding: "0 24px"
    height: "44px"
  button-inverse-hover:
    backgroundColor: "{colors.dusk-wash}"
  nav-link:
    textColor: "{colors.granite}"
    typography: "{typography.body}"
  nav-link-hover:
    textColor: "{colors.pine}"
  panel:
    backgroundColor: "{colors.birch}"
    textColor: "{colors.granite}"
    padding: "24px"
  manifesto-band:
    backgroundColor: "{colors.dusk}"
    textColor: "{colors.white}"
  footer:
    backgroundColor: "{colors.night-ground}"
    textColor: "{colors.night-ink}"
    padding: "64px 24px"
---

# Design System: Campground

## Overview

**Creative North Star: "The Trail Map"**

Campground's site is drawn like a survey map of good country: ruled edges, every fact under a label, routes numbered in order, and a horizon the words stand on. The map is where the brand's two halves meet. The outdoors supplies the warmth (Pine and Moss greens, a daylight campsite, a lantern-lit tent at night), and the cartography supplies the rigor (hairlines, a strict type scale, squared corners, nothing floating). A prospective client skimming the page should be able to read it the way they would read a trailhead sign: what is here, how far, which way.

The page is read from morning to night. The ground darkens as the visitor descends: Birch day in the hero, white and sunken working sections, purple arriving as dusk in the timeline, a night band, a Dusk-drenched manifesto, and a night footer. Illustration is the ground the text stands on, not a picture beside it: flat, faceted, hard-edged plates in the palette of the section they sit in, with the sky left as the section's own flat surface so every word sits on plain ground.

Components are **sturdy and plainspoken**. They are built like gear: squared, legible, full-weight fills, strong outlines where an outline is needed, no ornament. Warmth comes from the copy, the color, and the illustration plates, never from soft shapes or decorative effects. The system is flat by construction. It rejects the stock Tailwind UI look (default indigo, default grays, unmodified marketing blocks), gradient washes, glassmorphism, the "text left, image right" band repeated down a page, and literal summer-camp pastiche such as clip-art tents or faux-wood texture.

The tokens are generated by the Campground Design System into `_tailwind/campground.css`; that file is the source of every value below and is not hand-edited. This document describes how the shipped site uses them.

**Key Characteristics:**
- Flat surfaces separated by 1px lines; depth is a surface step, not a shadow.
- Slab-serif display (Arvo) over a grotesque body (Archivo), with wide uppercase labels (Archivo Expanded) naming everything.
- Green colourway by default; purple and night are per-section themes set with `data-theme`, not a user dark mode.
- Illustrations are full-bleed plates anchored to the bottom of a band; the text column stays on the band's flat surface.
- Corners are 2px. Nothing is rounder than 4px.
- A topography contour field appears in two places only (the manifesto band, the services panel), always under 10% opacity.
- 44px minimum target height on every control.

## Colors

A restrained light ground with one deep green doing the work, a second brighter green reserved for labels, purple entering as dusk (a timeline accent, then one fully committed Dusk band at the close), and two night surfaces in periwinkle.

### Primary
- **Pine** (`pine`): the brand's deep green. Primary buttons on light ground, the active-section marker in the header, link and focus color, nav hover. It is `brand-600` / `brand-deep` in the green theme. Pine is a control and a rule; it is never a ground.
- **Pine, pressed** (`pine-hover`): hover state for Pine fills.
- **Pine Tint** and **Pine Wash** (`pine-tint`, `pine-wash`): pale greens. Pine Tint is the text-selection color; Pine Wash is reserved for tinted fills.

### Secondary
- **Moss** (`moss`): the bright green, used only for uppercase labels and eyebrows on light green-theme surfaces. It was chosen over the logo's lighter green because that one fails AA on white.
- **Moss, inverse** (`moss-inverse`): Moss for dark grounds (a token; unused on the shipped page).

### Tertiary
- **Dusk** (`dusk`): the purple colourway's deep tone, `brand-600` inside `data-theme="purple"`. The timeline's rail and square nodes, the manifesto band's full drench, and the inverse button's text on that band. **Dusk, pressed** (`dusk-hover`) is its hover step.
- **Dusk Label** (`dusk-label`): the purple theme's label tone (`brand-bright`). Eyebrow and step numerals in the timeline section.
- **Dusk Pale**, **Dusk Tint**, **Dusk Wash** (`dusk-pale`, `dusk-tint`, `dusk-wash`): the purple theme's `brand-200`, `brand-100`, `brand-50`. On the Dusk band: the eyebrow, the lead paragraph, and the inverse button's hover fill.
- **Lantern** (`lantern`) and **Lantern Bright** (`lantern-bright`): the night theme's periwinkles. Lantern fills the button and colors links inside a night band; Lantern Bright sets night labels and inks the manifesto band's contour field.
- **Ember** (`ember`): the night theme's danger tone. Its one use is the heart in the footer's "Built with love in Colorado".
- **Night Ground**, **Night Raised**, **Night Line**, **Night Muted**, **Night Ink** (`night-ground`, `night-raised`, `night-line`, `night-muted`, `night-ink`): the night theme's surface, raised surface, hairline, supporting text, and text.

### Neutral
- **Granite** (`granite`): body and heading ink. Taken from the logo's wordmark gray, so text and logo match. Client logos are set in Granite via `currentColor`.
- **Granite Muted** (`granite-muted`): supporting copy, descriptions, summary lines.
- **Birch** (`birch`): the page ground, a slightly green off-white. Also the fill of bordered panels that sit on a White section.
- **Birch Sunken** (`birch-sunken`): the recessed band (Expertise).
- **White** (`white`): raised surfaces: header, the Services and Clients sections, the inverse button.
- **Line** (`line`) and **Line Strong** (`line-strong`): the 1px hairline that divides everything, and the stronger outline for controls that need a visible edge.
- **Danger** and **Danger Tint** (`danger`, `danger-tint`): error text and its background on light ground.

### Named Rules
**The Moss Is For Labels Rule.** Moss appears on uppercase labels and nowhere else. It is never a fill, never body text, never a button. Inside a themed section the label color re-points with the theme (Dusk Label on purple, Lantern Bright on night); the rule follows the token, not the hue.

**The Faint Contour Rule.** The topography field stays under 10% opacity (6% on light, 8% on Dusk and night) so text reads against a flat surface. It appears in exactly two places: the manifesto band, inked in Lantern Bright, and the bordered services panel behind the flat lay. It marks a place as ground; it is not a texture to turn up or spread.

**The One Band Rule.** Exactly one section per page is drenched in a brand color, it is the close, and that color is Dusk. Pine is never a ground: everywhere on the page it is a control, a marker, or a rule.

**The Dusk Falls Once Rule.** Purple enters the page as evening and does not appear above the timeline. Its order is fixed: accent (timeline rail and nodes), drench (manifesto), then night (footer).

## Typography

**Display Font:** Arvo (with Rockwell, Georgia, serif)
**Body Font:** Archivo (with system-ui, sans-serif)
**Label Font:** Archivo Expanded Bold (with Archivo, system-ui, sans-serif)

**Character:** A rounded slab serif over a plain grotesque, echoing the logo's lowercase slab wordmark and its wide uppercase descriptor. Arvo is set at regular weight even at display sizes; it gets its presence from size, not boldness. All three faces are self-hosted from `assets/fonts/` under the OFL.

### Hierarchy
- **Display** (400, 56px/60px, -0.01em): page-level headlines. The homepage hero runs larger than the token, `clamp(44px, 5.2vw, 80px)` at line-height 1.03 and -0.035em, so it fills the first viewport; the manifesto headline runs `clamp(36px, 4.2vw, 64px)` at 1.1. Both are the page's two summits; everything else uses the token ramp.
- **Headline** (400, 40px/46px, -0.01em): section titles, one per section.
- **Title** (700, 22px/28px): step titles and client names. The only place Arvo goes bold.
- **Body Large** (400, 18px/28px): section lead paragraphs, in Granite Muted. Kept to about `max-w-2xl` (672px). The hero lead runs 18px, 21px from `lg`, at line-height 1.5/1.45, capped at 760px.
- **Body** (400, 16px/24px): descriptions, list entries, header nav links (semibold), the arrow link.
- **Body Small** (400, 14px/20px): technology names (semibold), footer text and footer links (semibold).
- **Label Large** (700, 14px/20px, 0.12em, uppercase): section eyebrows. The hero eyebrow runs 15px, 19px from `lg`.
- **Label** (700, 12px/16px, 0.12em, uppercase): fact labels, step numerals, panel eyebrows, button text. The hero button's label runs 15px.

### Named Rules
**The Label First Rule.** Every section and every fact is named by an uppercase label before anything else is said: the label gives the kind, the Arvo line gives the thing. A heading with no label above it is missing its map key. The label takes the section theme's label token: Moss on green, Dusk Label on purple, Lantern Bright on night, Dusk Pale on the Dusk drench (Moss fails AA on Dusk as it does on Pine).

**The Lowercase Summit Rule.** The page's single top headline is set in lowercase with no period ("software that holds up in the field"), matching the lowercase wordmark. Section headlines below it use sentence case with a period.

## Layout

One centered column. Below `lg` (1024px) it is capped at 1424px with a 24px gutter; from `lg` it becomes a proportional column, 87.5% of the viewport capped at 1600px with no padding, leaving 6.25% gutters on either side. Sections are full-bleed bands stacked edge to edge, each with 96px of vertical padding, 128px from `sm` (640px); the footer runs 64px, 96px from `sm`. Bands step between Birch, White, and Birch Sunken and are separated by a 1px Line; the night band, the Dusk manifesto and the night footer break the alternation on purpose. Every `section[id]` carries a 96px `scroll-margin-top` so anchors land below the sticky header; scrolling is smooth unless the visitor prefers reduced motion.

Inside a band, content is one of four models: a 12-column grid with a lead block in the left 3 or 4 columns and the body in the rest (timeline 4/8 with the lead sticky at 128px from the top; clients 3/9); a 7/5 split of lead beside a bordered panel (services); a lead block capped at `max-w-2xl` above a ruled list (expertise, and the services list in two columns from `md`); or a text column capped at 860px (hero) or `max-w-xl` (night band) standing on a full-bleed plate. Illustrated bands set a minimum height from `lg` (924px hero, 800px night) so the plate has room below the text; below `lg` the plate becomes an in-flow strip (260px, 340px from `sm`) under the stacked text. Grid gaps are 48px; steps in the timeline are 48px apart; spacing otherwise follows Tailwind's 4px scale with no custom steps. Lists are ruled rows with 16 to 28px of vertical padding, not cards.

## Elevation & Depth

The system is flat. Depth is expressed by stepping the surface (Birch page, White raised, Birch Sunken recessed; Night Ground and Night Raised in the dark) and by 1px Line borders. Illustration plates sit behind the text column on their own z-layer but cast nothing. No shipped element casts a shadow.

### Shadow Vocabulary
- **Raised** (`box-shadow: 0 1px 2px rgba(39, 42, 53, 0.08), 0 4px 12px rgba(39, 42, 53, 0.08)`): the one shadow token the design system defines. Unused on the site so far; reserved for things that genuinely float over content, such as a menu or dialog. The mobile disclosure menu does not use it: it is in flow under the header, divided by a 1px Line.

### Named Rules
**The Lines Not Shadows Rule.** A panel is separated from its ground by a 1px Line and a surface step. If something in the page flow seems to need a shadow, it needs a border.

## Shapes

Squared. Controls take a 2px corner (`rounded-xs`); 4px (`rounded-sm`) is the ceiling, and panels, bands, and images take no radius at all. Borders are 1px in Line, with two deliberate exceptions at 2px: the Pine marker under the active nav link and the Dusk rail of the timeline. Nodes on that rail are 12px squares; the mobile menu's active marker is a 10px square. Dividers are full-width horizontal rules between rows, or 1px vertical Lines between columns; there are no pills, circles, or clipped shapes. The logo's angular twin-peak mark sets the geometry: sharp, faceted, no curves, and the illustration plates repeat it in their peaks.

### Named Rules
**The Two Pixel Rule.** 2px on controls, 4px at most, 0 on containers. The design system's own note on the scale is "use nothing rounder". Markers and rails are also 2px, and a marker is a square or a rule, never a dot.

## Components

Sturdy and plainspoken: squared, legible, full-weight, unornamented.

### Buttons
- **Shape:** squared with a barely eased corner (2px), 44px minimum height, 24px horizontal padding.
- **Primary:** Pine fill, white text set in Label (Archivo Expanded, 12px, uppercase, 0.12em). The same words, "Start a project", appear in the header (48px tall, 52px from `lg`), the hero (54px tall, 32px padding, 15px label), the clients "Next" panel (full width), the night band, and the manifesto band.
- **Inverse:** White fill with Dusk text, for the Dusk manifesto band only. Hovers to Dusk Wash.
- **Hover / Focus:** hover steps the fill to its pressed tone with no transition. Focus is a 2px outline, offset 2px, in the button's own color (white on the Dusk band). The document-wide focus outline color follows the theme's `--focus` token.
- **Night:** inside a `data-theme="night"` band the same classes resolve to a Lantern fill with near-black text.

### Text Links
- **Style:** Body, semibold, Granite, with a trailing arrow (`→`), hovering to Pine; 44px tall. Used as the quiet second action beside a primary button (18px in the hero).
- **On Dusk:** white, underlined with a 4px offset.
- **In the footer:** the email link resolves to Lantern.

### Bordered Panel
- **Character:** the trail marker. A Birch panel with a 1px Line and no radius, placed on a White section: 24px padding, 32px from `sm`.
- **Uses:** the services panel, which also carries a faint Pine contour field and the flat-lay plate (capped at 440px wide); and the clients "Next" panel (256px wide from `lg`), holding a Label eyebrow, a Body line, and a full-width primary button.

### Ruled List
- **Style:** a definition list of rows with 20px vertical padding (28px for the two-part expertise rows), a 1px Line above each row and below the last. Label in the theme's label color, description in Granite Muted. This is the default way to present a set of parallel items; it replaces the icon-card grid. The services list runs two columns from `md` with a 48px gap.

### Expertise Row
- **Style:** a ruled row split 3/9 from `md`: Label left, a wrapping list of technologies right (40px between, 24px between wrapped rows). Each technology is a monochrome inline SVG logo, 32px tall, centered above its name in Body Small semibold, with a 10px gap.

### Timeline
- **Character:** the route, numbered. An ordered list inside a `data-theme="purple"` section, with a continuous 2px Dusk rail down the left and a 12px Dusk square node at each step; the rail runs from the first node to the last, not beyond. Each step is indented 40px: numeral label ("01") in Dusk Label, a Title, and a Body paragraph capped at `max-w-xl`; 48px between steps. The lead block sits in the left 4 columns and is sticky from `lg`.

### Client Columns
- **Style:** three equal columns from `md`, divided by 1px vertical Lines with 24px of padding, the row ruled above and below. Each column holds the client's monochrome logo in Granite (36px tall, `fill: currentColor`), the name in Title, and a one-line summary in Body, Granite Muted. Below `md` they stack as ruled rows. The "Next" bordered panel sits as a narrower fourth column from `lg`.

### Navigation
- **Style:** a sticky White bar, 80px tall (96px from `lg`), with a 1px Line beneath. Logo left (44px tall, 56px from `sm`, 72px from `lg`), five Body semibold links in Granite hovering to Pine, primary button right. The active section carries `aria-current="true"` and a 2px Pine rule across the link's full width at its bottom edge; the rule fades in over an opacity transition, removed under reduced motion. Services is marked while the hero is in view. Driven by a scroll-spy of about thirty lines with no library; without JavaScript the links are plain anchors and no marker shows.
- **Mobile:** below `md` the links move into a disclosure menu opened by a 44px hamburger (Heroicons `bars-3` / `x-mark`, 24px, 1.5 stroke). The menu is a White panel under the bar with 56px ruled rows; the active row turns Pine and takes a 10px Pine square at its right. Below `sm` the primary button moves inside the menu as a full-width 48px control. Body scroll locks while open; Escape closes and returns focus to the trigger.

### Illustration Plates
- **Character:** the ground the words stand on. A wide flat panorama in the section's own palette, sky left transparent so the band's surface shows through, anchored to the bottom of the band and bleeding off left, right and bottom.
- **Hero:** daylight campsite (faceted twin peaks, treeline, still lake, one tent, a thread of smoke) in Pine, Moss and Pine Tint on Birch. Absolute from `lg`, 704px tall, object-fit cover anchored bottom; eager-loaded with `fetchpriority="high"` and preloaded from the head.
- **Night band:** the same campsite at night in Night Raised and the Lantern ramp, with a lit tent, stars and moon; absolute from `lg`, 560px tall, the text column clearing it with 360px of bottom padding; lazy.
- **Services flat lay:** a tent seen from above with six gear pieces (one per service), on a transparent ground inside the bordered panel; lazy, with a real `alt` because the gear carries meaning.
- **Format:** WebP at 2x layout size (panoramas under 200 KB, the flat lay under 40 KB), each with intrinsic `width`/`height`, `decoding="async"`, and `aria-hidden` (empty `alt`) when decorative. PNG masters and `.json` prompt sidecars live beside the plates for provenance and are excluded from the build. Any new plate is generated flat and faceted with hard edges; no painterly softness, blur or grain.

### Night Band
- **Character:** a full section with `data-theme="night"`, which re-points every token: Night Ground surface, Night Ink text, Lantern controls, Lantern Bright labels. It carries the "we're on watch" message on a `max-w-xl` text column standing on the night panorama. It has no contour field. It is a place in the page, not a dark-mode toggle.

### Manifesto Band
- **Character:** the one drenched close. A `data-theme="purple"` section filled with Dusk (`bg-brand-600`), with the contour field inked in Lantern Bright at 8%. Eyebrow in Dusk Pale, headline in white at the manifesto display size within `max-w-3xl`, lead in Dusk Tint within `max-w-xl`, then the inverse button beside an underlined white email link. No illustration: the night band above already carries the tent.

### Footer
- **Style:** `data-theme="night"`: Night Ground, 1px Night Line above, Night Ink text. From `md` a 12-column grid split 5/4/3: the Night lockup (48px tall) with a one-line description and "Built with ♥ in Colorado" in Body Small, Night Muted, the heart a 16px Heroicons solid heart in Ember with `sr-only` "love"; a "Sections" ruled link column with a Lantern Bright label, six Body Small semibold links at 44px each hovering to Lantern; and the email link in Lantern with the copyright, right-aligned. Below `md` the columns stack with 40px between.

## Do's and Don'ts

### Do:
- **Do** use the design system's tokens (`brand-*`, `surface`, `ink`, `ink-muted`, `line`, `font-display`, `font-label`, `text-label`, `text-display-lg`) and rename `indigo-` to `brand-` on any pasted Tailwind UI markup, even though the alias makes it render on-brand.
- **Do** put an uppercase label above every section title and every fact, in the section theme's label token.
- **Do** separate surfaces with a 1px Line and a surface step.
- **Do** keep every control at least 44px tall with a visible 2px focus outline.
- **Do** set a themed section with `data-theme="purple"` or `data-theme="night"` on the section and let the tokens re-point; don't hand-pick dark or purple colors.
- **Do** present parallel items as ruled rows, ruled columns, or a railed timeline.
- **Do** put an illustration behind the text column as a bottom-anchored plate with the sky left as the section surface, and keep every word on plain ground.
- **Do** ship raster plates as WebP at 2x with intrinsic dimensions, and keep the PNG master and prompt sidecar beside them for provenance.

### Don't:
- **Don't** round anything past 4px, or put a radius on a panel, band, or image.
- **Don't** add shadows to in-flow elements, and don't add gradients, glass, or blur anywhere.
- **Don't** use Moss for anything but labels, or the logo's light green (`#70aa43`) for text: it fails AA on white.
- **Don't** raise the contour field's opacity to 10% or beyond, or add it to a third place.
- **Don't** drench a band in Pine, and don't use purple above the timeline.
- **Don't** animate anything beyond the nav marker's opacity and the disclosure menu; no scroll-triggered motion.
- **Don't** ship a block that reads as stock Tailwind UI: default indigo, default gray scale, a gray hero with three icon cards, or a text-left image-right band repeated down the page.
- **Don't** illustrate with clip-art camping props or faux-wood and canvas textures. The three plates (day panorama, flat lay, night panorama) and the contour field are the whole outdoor vocabulary; the two retired SVGs (`tent-flat`, `backpack-flat`) stay in the repo as reference for the vocabulary.
- **Don't** hand-edit `_tailwind/campground.css`; change the tokens in the Campground Design System and re-export.
