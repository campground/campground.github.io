# Campground — Product Context

Design context for anyone (human or agent) doing design work on this site.
Read this before designing; update it when the answers change.

<!-- impeccable:product-schema 1 -->

## Platform

web

## What it is

Campground is a full-service digital agency and consultancy. This repo is its
public site, <https://www.campgrounddd.com>.

## Positioning

Small and senior. Clients work directly with the principals who do the work,
with no account layers between them and the people designing and building.

## Services

Six services, the same map DockYard (<https://dockyard.com/services>) uses;
we do the same work. Named on the site in this order and this wording:

- **Strategy + discovery** — research, product definition and a roadmap the
  client can budget against.
- **Web + mobile apps** — design and engineering: Rails, TypeScript and React
  on the web; React Native for iOS and Android; Elixir where uptime and scale
  matter most. Includes brand and identity, product and app UI, and sites the
  client's team can update without a developer (content management is part of
  this, not a separate service).
- **AI automation** — practical AI inside the product and the operations:
  workflows that run themselves, and measurement to prove it.
- **Consulting + team augmentation** — senior engineers who join the client's
  team, ship from the first week and leave the codebase better than they found
  it.
- **Architecture reviews + audits** — a second set of senior eyes on code and
  infrastructure: what will break under load, what to fix first, in writing.
- **Application maintenance** — ongoing support after launch: updates,
  security patches, performance checks and the next release, on a retainer
  sized to the product. Includes uptime and error monitoring around the clock
  and an on-call engineer who already knows the code.

**Expertise strip** (after services, DockYard's "Expertise across
technologies" as the model): application stack is Ruby on Rails, React,
React Native, Elixir; cloud and hosting is Fly.io, AWS, Azure. Logos are
monochrome inline SVGs in `_includes/logos/` (Simple Icons for Rails, React,
Elixir, Fly.io; Wikimedia Commons for AWS and Azure; React Native is the React
atom in a phone frame, drawn here).

Claims cleared for publication: working software every two weeks, one working
day reply time, senior people with no account layer, on-call after launch.

## Audience

Prospective clients evaluating whether to hire the agency: founders, product
leaders, and operations leads. They arrive from a referral, a link, or a
search, skim fast, and want to know: what does Campground build, is it good,
and how do I get in touch. AI-automation buyers may be less technical than
app-development buyers; write for both.

## Job of the site

1. Say what Campground does, in one screen.
2. Prove it with work.
3. Make contact effortless.

## Brand personality

Three traits, held in tension:

- **Warm, outdoorsy, crafted** — the campground metaphor is the brand. Earthy,
  tactile, friendly. A place people gather.
- **Bold, playful** — big type, confident color, visible personality. Not a
  template agency site.
- **Technical, precise** — the craft is real engineering. Sharp alignment,
  systematic spacing, fast pages, clean markup.

Resolve conflicts in this order: precise structure underneath, bold expression
on top, warmth in the details (copy, color, texture). Playful never means
sloppy; outdoorsy never means kitsch (no clip-art tents, no faux-wood textures).

## Tone of voice

Plain, friendly, direct. Short sentences. Confident without agency-speak
("we craft bespoke digital experiences" is banned). A little campfire humor is
welcome; jargon is not.

## Brand assets

Logos live in `assets/logos/` (PNG). Vector masters (`.ai`, `.eps`) are kept
outside the repo in `~/Downloads/Campground-Logos`; export SVGs from those
before launch.

- **Mark:** angular twin-peak mountain — a dark outline peak over lighter
  faceted peaks. Sharp, geometric, no curves.
- **Wordmark:** lowercase "campground" in a rounded slab serif, with a
  wide uppercase sans descriptor beneath.
- **Lockups:** `Digital` ("campground DIGITAL"), `Design`
  ("campground DESIGN + DEVELOPMENT"), and `Icon` (mark only). Each in green
  and purple.

**Primary lockup: `Digital`, green.** Green is the primary brand color; purple
is the accent. The `Design` lockup and purple variants are secondary.

Colors sampled from the logo files:

| Role          | Green set (primary) | Purple set (accent) |
| ------------- | ------------------- | ------------------- |
| Dark          | `#006636`           | `#332d70`           |
| Light         | `#70aa43`           | `#775fa8`           |
| Wordmark text | `#3d3f44`           | `#272a35`           |

The logo typefaces are not identified; the web pairing that echoes them is
Arvo (display), Archivo (body) and Archivo Expanded Bold (labels), self-hosted
in `assets/fonts/` under the OFL.

## Design system and tooling

- **Campground Design System** (claude.ai artifact,
  <https://claude.ai/artifact/4LqjCesA8rLnPqGdk9bucq>) is the source of truth:
  tokens, green/purple/night themes, re-skinned Tailwind UI blocks, logos,
  illustrations, the topography pattern and site copy. Its generated stylesheet
  is vendored at `_tailwind/campground.css`; read its README before designing.

- **Tailwind CSS** with **Tailwind UI** (Pro account, signed in via the
  browser) as the component starting point. Use the HTML variants; this is a
  static Jekyll site, not React.
- **Heroicons** for icons, **Hero Patterns** for background texture.
- **Build our own theme.** Tailwind UI supplies structure, not the look. Use
  the design system's tokens (`brand-*`, `surface`, `ink`, `font-display`,
  `text-label` …) and its re-skin swaps on every component. A page that reads
  as stock Tailwind UI is a failure: default indigo, default gray scale, and unmodified marketing blocks
  are all out.

## Anti-references

- Generic agency template: gray hero, stock photo, three icon cards.
- AI-slop defaults: purple gradients, glassmorphism, Inter-on-white, centered
  everything. (Brand purple is fine; purple-to-pink gradient washes are not.)
- Literal summer-camp pastiche.

## Technical constraints

- Jekyll, hosted on GitHub Pages at `www.campgrounddd.com` (see `README.md`).
- Deployed by GitHub Actions (`.github/workflows/pages.yml`): Tailwind CLI
  compiles `_tailwind/site.css` to `assets/css/site.css`, then Jekyll builds.
  The compiled CSS is not committed.
- No gem theme (`theme: null`); layouts live in `_layouts/`.
- Static only. Minimal JavaScript, and only where a Tailwind UI component
  needs it (mobile nav, disclosure).
- Accessibility: WCAG 2.1 AA — contrast, keyboard navigation, reduced motion.
  Check brand colors for contrast before using them on text: `#70aa43` on
  white fails AA for body text.

## Open questions

- Case studies: none on hand yet. Client names and testimonials exist and are
  cleared to publish, but the text is not in this repo. Wait for the real
  material; never write placeholder quotes, client names, or metrics.
- Contact path: email link, form, or booking link.
- Logo typefaces, if known, and whether to license them for the web.

`DESIGN.md` (with `.impeccable/design.json`) records the shipped visual system;
the design system artifact above remains the token source it is derived from.
