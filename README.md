# Gift file

Two gift lists in one GitHub Pages site: one for Bence Tanko-Bartalis, one for Maria.

- `index.html` is the hub. It carries the CSS-only filter that shows all gifts, only Bence's,
  or only Maria's. No JavaScript, no external requests.
- `slippers.html` is gift 01 for Bence: Totes Toasties men's moccasins, navy, £16.99 at TK Maxx,
  Medium box (UK 8-9 / EU 42-43). Every fact on it comes from the photo Bence took in store.
- `hair-trimmer.html` is gift 02: cordless trimmer with adjustable parts, for the sides of his hair,
  not a full kit. Brief only, no brand, model or price. `haircut-kit.html` is a meta-refresh
  forwarder to it, kept so the old link does not die.
- `packable-backpack.html` is gift 03: spare bag, about 20 litres, rugged enough for heavy shopping,
  Osprey preferred but not required. Brief only, no model or price.
- Maria's list is empty by design until an idea is filed.

Live: https://percyblackassistant-cpu.github.io/gift-idea/

## The rule for this site

Only put on a page what Bence actually said or what was seen in a real listing with a date.
When something is missing, say it is missing and ask him. Never fill a gap with a plausible
brand, price, spec or stock claim: an invented £36.99 reads exactly like a checked one.

`assets/` holds the resized store photo and the line illustrations. The original 4000x3000 photo
stays outside the repo (`~/workspace/gift-site-src/gift-source.jpg`). Deploys run on push to
`main` via `.github/workflows/deploy.yml`.

Adding a gift: take the brief as given, write a detail page in the same shape, then add a card to
the matching list in `index.html` and bump both counts. The filter picks cards up by the section's
`data-for` attribute, so nothing else needs touching.
