# Cursor Reveal Portfolio

A one-page portfolio for Sandeep Komal Pothu (cloud, DevOps and DevSecOps). The hero shows a racing-style helmet; move the cursor over it and a soft, wobbly blob follows, unmasking the face underneath. The rest of the page reads like a delivery pipeline.

**Live:** https://sandeepkomal.github.io/Cursor-Reveal-Portfolio/

## Sections

1. **Hero:** the cursor-reveal portrait (helmet → face)
2. **About:** manifesto and four principles (Cloud, Platform, Delivery, Security)
3. **Stack:** tools laid out as pipeline stages: Code → Build → Scan → Provision → Run → Observe
4. **Work:** project cards with a cursor spotlight and a small "deploy history" chart
5. **Journey:** career told as a `git log`
6. **Contact:** email (with copy button), LinkedIn, GitHub and Medium

## Effects

- **Cursor reveal:** a wobbly blob follows the cursor and unmasks the face behind the helmet.
- **Scroll unmask:** scrolling past the hero opens the visor and reveals the whole face.
- **Text scramble:** the headline boots up from terminal characters, and replays on hover.
- **Custom cursor:** a trailing ring that grows on links and shows "VIEW ↗" on project cards (mouse only).
- **Pipeline run:** stages tick to ✓ one by one as you scroll through the stack.
- **3D tilt:** project cards tilt toward the cursor with a soft glare.

All effects switch off for visitors who prefer reduced motion, and the cursor and tilt are skipped on touch screens.

## How it works

- Plain HTML, CSS and JavaScript in one file (`index.html`). No frameworks, no libraries, no build step.
- The helmet is drawn in code on a `<canvas>` on the same 1000×1000 grid as `avatar.png`, so the two line up. The avatar shows through an animated blob mask (layered sine waves, stretched in the direction of movement, with three trailing copies) using `source-in` compositing.
- Light and dark themes follow the system setting. Reduced-motion is respected, touch works and the layout holds down to phone width.

## Editing

- Text, projects and links are plain HTML in `index.html`.
- The `CONFIG` block near the bottom sets the portrait: `revealSrc` (the face), `baseSrc` (optional photo instead of the drawn helmet) and `fit`.

## Run locally

Open `index.html` in a browser, or serve the folder with `python3 -m http.server`.

## Credits

All code and the helmet artwork are original. Fonts: Bricolage Grotesque, Instrument Sans and JetBrains Mono via Google Fonts (SIL Open Font License).
