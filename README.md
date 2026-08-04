# AppADay 089 - Ink Trace

Type a short phrase and watch it write itself as a single-stroke ink drawing, one pen path at a time. Restyle it freely, share the exact look with a link, and export it as a still image or a full animation.

Live: https://augustineiacopelli.github.io/appaday-089-ink-trace/

Part of AppADay: https://augustineiacopelli.github.io/appaday/

## What it does

Ink Trace renders whatever you type as genuine pen strokes rather than a font on a page. Every letter is traced along its true drawing path, stroke by stroke and left to right, so the phrase appears the way a hand would write it. Longer phrases wrap onto centered lines, and the whole composition scales to fill the paper. Press Trace or Enter to replay the animation at any time.

## How it works

The lettering is built on the public-domain Hershey vector fonts, a set of single-stroke glyphs where each character is a series of pen paths instead of a filled outline. The app parses that coordinate data at load time, lays the glyphs out into SVG paths, and animates the drawing by advancing each path's stroke dash offset in sequence. Because the strokes are real geometry, the same paths drive the on-screen SVG, the exported vector, and the frame-by-frame video, so what you see is what you get in every format. There is no build step, no framework, and nothing leaves the browser.

## Styling

Five scripts are included, from a clean single-stroke sans through a roman serif, a flowing script, a connected cursive, and a blackletter gothic. Ink and paper each offer a set of presets plus a full custom color picker, and the paper grain adapts its speckle to light or dark stock automatically. Stroke weight, draw speed, and the nib shape (a round brush or a flat chisel) are all adjustable, and a rough inked finish adds a subtle hand-drawn wobble to every stroke. Your settings are remembered between visits.

## Sharing and export

The current phrase and every style setting are encoded in the page link, so Copy link hands someone the exact piece you made, reproduced the moment they open it. You can export a still as a crisp PNG or as clean vector SVG, and the paper grain and inked finish bake into both. The Video button records the trace animation to a WebM file, ready to drop into a message or a slide.

## Technical notes

One self-contained HTML file of vanilla HTML, CSS, and JavaScript. The only external resource is Google Fonts for the interface type. No AI, no accounts, no network calls with your content. All source is ASCII-clean and every drawing, export, and preference lives entirely on your device.
