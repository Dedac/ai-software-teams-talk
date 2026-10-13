# Are Traditional Software Teams a Thing of the Past?

The deck is published at <https://dedac.github.io/ai-software-teams-talk/>
by the `.github/workflows/pages.yml` workflow whenever `presentation/` changes
on `main`.

Open [`index.html`](index.html) in a browser. No build, server, or internet
connection is needed; the fonts are bundled locally. Keep the `assets/` folder
next to the HTML file when sharing the deck.

The 43-slide deck follows the [repository outline](../README.md), with a
high-contrast Midnight background, green accent, Hubot Sans headlines, and
Mona Sans body text. Large headlines and sparse slide copy are designed for
projection to a large audience. The final source slide is an appendix.
Slides 8 and 9 introduce the RPI-to-QRSPI+ evolution and compare the workflow
paths; the QRSPI+ diagram shows the full route, with quick-fix details in notes.
Slides 25–27 cover the hard parts of running agentic engineering systems, and
slide 28 maps the talk onto GitHub's Agentic Engineering System (AES).
Slides 29–32 open the people-and-teams section with "You've been promoted to
manager."

## Presenting

| Key | Action |
| --- | --- |
| Right arrow, Space, Page Down | Next slide |
| Left arrow, Page Up | Previous slide |
| Home / End | First / last slide |
| Number keys | Jump to a slide; type multiple digits within 650 ms |
| G | Toggle clickable slide overview |
| N | Toggle presenter notes |
| F | Toggle fullscreen, where the browser permits it |
| Escape | Close overview or notes |

Slide links use hashes, for example `index.html#16`. The on-screen controls
also support navigation, overview, notes, and fullscreen.

**Notes are visible on the same screen when enabled.** Do not turn them on
while sharing that screen with the audience. Review them beforehand or print
the outline separately. They contain delivery cues, source links, and research
caveats; this is not a separate-window presenter console.

Prepare the BeamRS demo or recording separately and switch to it from the
second slide, before continuing to the thesis. Enterprise examples remain anonymized.
Case figures trace to the supplied outline; the only research figures
on slides are METR's, checked against METR's own posts, with study-scope
caveats in the notes.

## PDF export

Use the browser's **Print > Save as PDF**, enable **background graphics**, and
disable browser headers and footers. The print stylesheet makes every slide a
1280 x 720 page, independent of the current slide, overview, or notes mode.
The resulting PDF includes the source appendix but excludes presenter notes
and navigation controls.

## Fonts

Bundled Latin fonts: Mona Sans and Hubot Sans from Fontsource, and Monaspace
Neon from Fontsource. Their SIL Open Font License texts are in `assets/`.
The deck engine uses only inline CSS and vanilla JavaScript.
