# Asset credits

## Line-art figure (Today hero, onboarding welcome, return welcome, milestone)

| File | What it is | Source / licence |
|---|---|---|
| `img/lineart-figure.svg` | Faithful vector of the client's single-line figure drawing. It was traced with potrace and not simplified or redrawn. It is filled with `currentColor` so the app can show it in plum-ink on the light panels and in ivory on dark stages. | **Supplied by the client. Licence to be confirmed.** The source file is `references/lineart-reference.png`. It came without licence or author information, and it looks like a stock vector, so confirm the licence before any public release. |
| `img/lineart-figure.png` | The same artwork with the white background removed, using the original pixels: alpha comes from luminance and the colour is set to plum-ink #2E1B2A. It is cropped to the figure. | Same as above. |

**Fidelity check for the vector**, run at the original 1600 × 1920 size with the vector rasterised and overlaid on the PNG:

- 100% of the original's ink pixels lie within 1 px of the vector's ink.
- 100% of the vector's ink lies within 1 px of the original's ink.
- 99.83% of all visible original pixels, including faint antialiasing, lie within 1 px of the vector.
- The ink masks overlap with an IoU of 0.96.
- The mean grey difference is 0.34/255.

The trace used 3× supersampling, a threshold of 140/255, turd size 4 and potrace's default curve fitting (alphamax 1.0, opttolerance 0.15). The overlay images are saved in the verification folder.

**How the app uses it:** the artwork is never redrawn. The draw-on reveal uses an SVG mask of thick strokes that roughly follow the pen's path, then a soft full-mask fade. The crops are full figure on Today, head and shoulders on onboarding and return (mirrored on return), and face only on the milestone.

**Other line art:** the brief asked for 2–4 more freely licensed single-line figures from sources such as Openverse, Wikimedia Commons, SVG Repo, rawpixel, Vecteezy and Freepik. None of those hosts could be reached from this environment, because the network policy refused the connections. No third-party artwork was used. The other moments reuse the client's drawing in different crops and orientations, as instructed.

## Photographs

All photographs come from the **Open Images Dataset** (Google). It redistributes Flickr photos that their authors published under **Creative Commons Attribution 2.0** (CC BY 2.0, https://creativecommons.org/licenses/by/2.0/). The image files were downloaded from the dataset's public mirror (`open-images-dataset.s3.amazonaws.com`, 1024 px on the long edge).

**Changes made (as CC BY requires us to say):**

- Each photo was colour-graded to the app palette: gentle desaturation, plum-lifted shadows and ivory highlights.
- The black-and-white photos got a plum-to-ivory duotone.
- All were re-encoded as WebP and may be cropped on screen.
- Nothing else was altered.

**Release caveat:** CC BY covers copyright only. It does not include model releases for the people pictured. Production use needs release-cleared or commissioned photography.

**Removed in round 2:**

- "Rodeo Cove: III" (the figure crouching on the hillside, the previous Today hero) was removed because the client found it off-tone.
- "Do I Need to wait?" (a sad figure at a window, on the Care card) was removed for the same reason.
- "West Iceland: X" is no longer used.
- An interim cut-out portrait from Open Images 000a98aa78afeb18 ("scan0612", Jorge Goicochea) was replaced by the client's line art and is not shipped.

| File | Used for | Title / author | Source (Flickr page) | Open Images ID | Licence |
|---|---|---|---|---|---|
| `img/return-jetty.webp` | Care: "Having a hard week?" card | "Paseando al perro bajo la Luna.", Gabriel Villena | https://www.flickr.com/photos/gvillena/3623056747 | 7ec2174195ad57c6 | CC BY 2.0 |
| `img/milestone-shore.webp` | Milestone share card | "ke'e", Matt MacGillivray | https://www.flickr.com/photos/qmnonic/4113415477 | 9082612f962e9ccb | CC BY 2.0 |
| `img/plateau-path.webp` | Month-two plateau reframe | "DSC_0401", Pavel Dobrovsky | https://www.flickr.com/photos/lukecz/15221475416 | 5d4cba58500bc361 | CC BY 2.0 |
| `img/two-walkers.webp` | Week-one companion | "Alexandra Palace", Brian Adamson | https://www.flickr.com/photos/66391503@N00/10509010385 | 6f27684d67a68b4a | CC BY 2.0 |
| `img/footprints.webp` | Progress: week by week | "L'homme qui marche", esyckr | https://www.flickr.com/photos/lifestar/6132959519 | 22aca783bb6470af | CC BY 2.0 |
| `img/fog-beach.webp` | Progress: photos row | "Photographer in the Mist", Ingrid Taylar | https://www.flickr.com/photos/taylar/5231086360 | 1f191fe56302bcf5 | CC BY 2.0 |

Author profile pages are at `https://www.flickr.com/people/<name>/` for gvillena, qmnonic, lukecz, 66391503@N00, lifestar and taylar.

## Brand

| File | What it is | Source / licence |
|---|---|---|
| `brand/logo-black.svg`, `brand/logo-white.svg` | The lowercase "pomegranate" wordmark, recreated as outlined paths with no font dependency | Set in **Bodoni Moda** (opsz 28, weight 600, tracking −1.2%) by Owen Earl (indestructible type*), SIL Open Font License 1.1, https://github.com/google/fonts/tree/main/ofl/bodonimoda. The outlines were generated with fontTools and HarfBuzz. This is a stand-in for the client's own wordmark artwork. |

## Typefaces loaded by the app (Google Fonts, SIL OFL 1.1)

- **Geist** (Vercel) for display and interface type, at weights 300, 400 and 500.
- **Geist Mono** for corner-pinned micro labels and figures in labels.
- **Newsreader** (Production Type) for the short book-serif sentences.
- **Bodoni Moda** appears only in the wordmark, as outlines; it is not loaded as a font.

The dot-matrix numerals are a custom 5 × 7 SVG grid drawn in code, not a font.
