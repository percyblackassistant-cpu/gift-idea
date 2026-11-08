# Gift file

Two gift lists in one GitHub Pages site: one for Bence Tanko-Bartalis, one for Maria.

- `index.html` is the hub. It carries the CSS-only filter that shows all gifts, only Bence's,
  or only Maria's. No JavaScript, no external requests.
- `slippers.html` is gift 01 for Bence: Totes Toasties men's moccasins, navy, £16.99 at TK Maxx,
  Medium box (UK 8–9 / EU 42–43).
- `haircut-kit.html` is gift 02 for Bence: Wahl Colour Pro cordless haircutting kit, £36.99 direct
  from Wahl, with the lithium kit and the Elite Pro as alternatives.
- Maria's list is empty by design until an idea is filed.

Live: https://percyblackassistant-cpu.github.io/gift-idea/

`assets/` holds the resized store photo and the line illustration for the hair kit. The original
4000×3000 photo stays outside the repo (`~/workspace/gift-site-src/gift-source.jpg`). Deploys run
on push to `main` via `.github/workflows/deploy.yml`.

Adding a gift: write a detail page in the same shape as `slippers.html`, then add a card to the
matching list in `index.html`. The filter picks cards up by the section's `data-for` attribute, so
nothing else needs touching.
