# Add Conferences Section with Embedded YouTube Talk

## Summary

This PR extends the personal landing page at [jaranas.io](https://jaranas.io) with a new **Conferences** section that showcases public talks. The first talk embedded is a recent presentation delivered in Spanish.

## Changes

### `index.html`
- Added a `#conferences` anchor link to the top navigation bar.
- Added a new `Conferences` section between the `Mentoring` and `Contact` sections.
- Embedded the YouTube talk using a fully responsive 16:9 iframe player (CSS `padding-bottom: 56.25%` technique), with rounded corners and a subtle border consistent with the existing card style.
- Added three new CSS utility classes:
  - `.talk` — grid container for the talk embed and its metadata.
  - `.talk-embed` — responsive wrapper for the YouTube iframe.
  - `.talk-meta` — styled card for the talk title and description.
- Talk featured:
  - **Title:** Junie, más allá de Claude Code ¡en nuestro entorno de confianza! 🇪🇸
  - **URL:** https://www.youtube.com/watch?v=3T_ehDPPYvI
  - The 🇪🇸 flag emoji indicates the talk is delivered in Spanish.

### `README.md`
- Updated the **Features** section to mention the new Conferences section.
- Added a note about the embedded YouTube player in the Conferences section.

## Design Decisions

- The section follows the same visual language as the rest of the page (dark card style, muted text, accent colors, border radius).
- The iframe uses `loading="lazy"` to avoid blocking page load.
- The talk description is written in English to keep the page consistent, while the original talk title is preserved in Spanish with the flag emoji as a language indicator.

## Testing

- Verified the section renders correctly at desktop and mobile widths (responsive grid collapses to single column below 860 px, consistent with existing breakpoints).
- Confirmed the YouTube embed loads and plays inline without layout issues.
