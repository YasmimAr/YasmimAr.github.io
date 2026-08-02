# yasmim.dev

Personal portfolio site. Live at [yasmim.dev](https://yasmim.dev)

## Stack

Vanilla HTML, CSS and JavaScript. No frameworks, no build step — for a single
static page, a framework would be dead weight.

## Notes

- The tabs follow the ARIA tablist pattern (roving `tabindex`, arrow keys,
  home/end), and inactive panels use `hidden="until-found"` with a
  `beforematch` handler. Find-in-page reaches text inside a closed tab, and the
  nav switches to that tab as the browser reveals it. The CSS deliberately
  never sets `display: none` on a panel — that would override the
  `content-visibility: hidden` the UA gives `until-found` content and kill
  find-in-page.
- Without JavaScript nothing can switch tabs, so a `<noscript>` block hides the
  nav and unhides every panel. The page degrades into one long document
  instead of three sections nobody can open.

## Running locally

Open `index.html` in a browser, or serve the folder with any static server.