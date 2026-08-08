# re-supply

Single-file landing page for a ReSupply Boston couch donation pickup service.

## Running it

No build step. Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8765
```

Then visit <http://localhost:8765/index.html>.

## Structure

Everything lives in `index.html` — markup, an inline Tailwind config, a small
components layer, and all JavaScript. Only assets sit beside it:

| Path | Contents |
| --- | --- |
| `animations/` | Lottie JSON for the pickup steps and the items illustration |
| `brands/` | Charity partner logos used by the marquee and review cards |
| `card-logo/` | Trustpilot, Google, BBB and ReSupply marks for the review bar |
| `icons/` | Brand icons for the three pickup-process steps |
| `lottie_light.min.js` | Lottie player |
| `Map_home-1.json` | Coverage map animation |

## Notes

- Styling uses the Tailwind **Play CDN**, which compiles in the browser. That is
  fine for previewing, but a production build should use the Tailwind CLI to
  emit a static stylesheet.
- Lottie animations play once as they scroll into view. A `data-lottie-stop`
  attribute pins an animation to a chosen frame — the items illustration uses it
  because its final frame is empty.
