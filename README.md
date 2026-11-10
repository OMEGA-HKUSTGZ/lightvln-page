# LightVLN — OMEGA Lab project page

Project page for **LightVLN: Efficient Aerial Vision-and-Language Navigation with Compact
Memory and History-Guided Local Aggregation**, in the OMEGA Lab style.

- Paper: <https://arxiv.org/abs/2610.05024>
- Code: <https://github.com/zhaoyiming/LightVLN>
- Page: <https://omega-hkustgz.github.io/projects/lightvln/> (live once the lab site lists it)

## Working on the page

The page is `index.html` plus `assets/`; there is no build step. Rules for agents are in
[`AGENTS.md`](AGENTS.md).

```sh
node tools/check.mjs     # what CI runs
node tools/serve.mjs     # look at it locally
```

Every pull request gets a preview link, posted on the pull request. A push to `main` asks the
lab site to republish.

## Sources

Everything on the page comes from public material. Keep this list current.

| On the page | Source |
| --- | --- |
| Title, authors, affiliation, text | arXiv 2610.05024v1 (4 Oct 2026). The text paraphrases the abstract and Sections III–IV; it adds no claims. |
| `overview.webp`, `architecture.webp`, `efficiency.webp`, `latency.webp`, `hil-rollout.webp` | Figs. 1–5 of the paper, rendered from the arXiv source PDFs at 2400 px wide (`pdftoppm`, then `cwebp -q 90`). `social.jpg` is Fig. 1 on a 1200 × 630 canvas for link previews. |
| OpenFly and AerialVLN-S tables, headline numbers, efficiency and campus numbers | Tables I and II and Section IV-D of the paper, copied from the LaTeX source. |
| `hil.mp4`, `offline-comparison.mp4` and their posters | The authors' own project page, linked from the code repository (files `hil.mp4`, `offline-comparison.mp4`, `hil-poster.png`, `simulation-poster.png`, fetched 2026-11-10; videos unmodified, posters converted to JPEG). The captions follow the authors' descriptions there: hardware-in-the-loop, and an offline simulation replay. |

Not on the page because no public material exists: real-world flight footage (the paper's
onboard evaluation is hardware-in-the-loop, with a stationary, disarmed aircraft), released
model weights, and the ablation tables (Tables III–V, left to the paper).
