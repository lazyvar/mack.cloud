# Light cloud redesign — design

Date: 2026-05-17

## Goal

Reskin and polish the single-page `index.html` landing page into a white/blue,
cloud-evoking theme. Keep the existing two-column links layout; improve color,
spacing, typography, and link styling. No new files, no new dependencies.

## Theme & color

- Background: fixed top-to-bottom sky gradient, pale white-blue (`#eef6ff`) at
  the top easing into a deeper sky blue (`#cfe6fb`) at the bottom.
- Text: deep slate-blue (`#1e3a5f`) replacing near-black — softer, still high
  contrast.
- Accent: keep `steelblue` for links and italics.

## Cloud touches (playful / literal)

- Soft, blurry white cloud blobs floating behind the content — pure CSS, large
  white radial-gradient shapes with blur and low opacity.
- The existing `assets/cloud.svg` header image stays, with a gentle drop-shadow
  so it lifts off the sky.
- Content sits on a semi-transparent white card with rounded corners and a soft
  shadow.

## Type & polish

- Switch body font to **Varela Round** (already self-hosted in `static/fonts`,
  currently unused). Drop the unused Source Serif Pro `@font-face` rules and
  preloads.
- Larger, friendlier `h1`.
- `Socials` / `Apps` section headers styled as small spaced labels.
- Link rows: keep label-left / link-right layout; add subtle row separators and
  a hover that faintly tints the whole row blue.
- More generous padding and spacing throughout.

## Scope of changes

- `index.html` — inline `<style>` rewrite, font-face cleanup, preload cleanup.
- `site.webmanifest` — `theme_color` / `background_color` to a blue tint.
- `browserconfig.xml` — `TileColor` to a blue tint.
- `index.html` meta — `theme-color` to match.

## Out of scope

- Layout restructuring beyond spacing/polish.
- New images, fonts, or build tooling.
