# Are Traditional Software Teams a Thing of the Past?

The deck is published at <https://dedac.github.io/ai-software-teams-talk/>
by the `.github/workflows/pages.yml` workflow whenever `presentation/` changes
on `main`.

Open [`index.html`](index.html) in a browser. No build, server, or internet
connection is needed; the fonts are bundled locally. Keep the `assets/` folder
next to the HTML file when sharing the deck.

The 44-slide deck follows the [repository outline](../README.md), with a
high-contrast Midnight background, green accent, Hubot Sans headlines, and
Mona Sans body text. Large headlines and sparse slide copy are designed for
projection to a large audience. The final source slide is an appendix.
Slide 2 introduces the broken software-engineering process; slide 3 opens the
people-and-teams section with "You just got promoted." Slide 4 asks what
agents make us now; slide 5 follows with the manager's responsibility for
team output. Slide 6 introduces BeamRS and the tools chosen to build it, and
slide 7 reveals its duplicated interface. Slides 13–19 tell the
workflow story in order: lessons, The Relay, the RPI-to-QRSPI+ diagram (slide
15, full route with quick-fix details in notes), the QRSPI+ case, the
comparison, and slide 19 on what comes next: reduced complexity, evaluation,
and review. Slides 20–21 ask how to prove a process change is better and how
to avoid overfitting the process to today's problems. Slide 22 returns to
BeamRS's tool choices and what local review found; slides 23–24 cover the
BeamRS pull request reviews, with the two-layer review setup in slide 23's
notes. Slide 25
closes the review loop; slides 26–27 introduce repository automation and its
authority boundaries. Slides 28–31 are a natural-language-uncertainty section:
every harness,
skill, and agent is more natural language, illustrated with an ambiguous
English sentence. Slides 32–33 cover the hard parts of running agentic
engineering systems, and slide 34 maps the talk onto GitHub's Agentic
Engineering System (AES), before the careers-and-teams section. The
special-thanks slide precedes Q&A and the source appendix.

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

Slide links use hashes, for example `index.html#12`. The on-screen controls
also support navigation, overview, notes, and fullscreen.

**Notes are visible on the same screen when enabled.** Do not turn them on
while sharing that screen with the audience. Review them beforehand or print
the outline separately. They contain delivery cues, source links, and research
caveats; this is not a separate-window presenter console.

Prepare the BeamRS demo or recording separately and switch to it on slide 6,
after the opening section, and stay on it through the slide 7 reveal before
continuing to the thesis.
Enterprise examples remain anonymized.
Case figures trace to the supplied outline; research claims are linked to
their sources in the outline and relevant speaker notes.

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
