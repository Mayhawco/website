# mayhawco.com — coming soon

Static, self-contained, no build step. Every asset is local: no CDN, no Google
Fonts request, no third-party anything. Nothing about a visitor leaves the server.

```
index.html          the page (inline SVG wordmark, inline CSS and JS)
fonts/              Fraunces (subset), Archivo, IBM Plex Mono — all self-hosted
og-image.png        1200x630 link preview
favicon.*  icon-*   from the brand package
CNAME               for GitHub Pages
```

## Deploying

Same pattern as the BDL sites — push this folder to a repo and turn on GitHub
Pages. `CNAME` is already set to `mayhawco.com`. In GoDaddy DNS, point the apex
at GitHub's four A records and `www` at the Pages hostname as a CNAME.

Or drag the folder onto Netlify or Cloudflare Pages, which is faster and gives
you HTTPS without touching A records.

**Before it goes live:** make sure `hello@mayhawco.com` actually exists as an
alias in Workspace. It's the only way anyone can reach you from this page.

## Details worth knowing

**The wordmark is inline SVG**, not text, so it renders identically everywhere
and needs no font to be loaded first. There is no flash of fallback type.

**Fraunces is subset to the 24 characters actually used** — instanced at
`opsz 144, wght 500, SOFT 30, WONK 1` and stripped to just the glyphs on this
page. 3 KB instead of 121 KB.

**The counter in the footer is real.** It works out how many days until May 1
and says so; through May it reads "Mayhaws are ripe" instead. Nothing to update.

**The atmosphere is a canvas** — three very wide, very low-opacity pools of warm
light drifting on cycles of 90 to 180 seconds, plus an SVG-turbulence grain
overlay. It should never be noticeable on its own; it exists so a flat dark
field has somewhere to sit. `prefers-reduced-motion` freezes all of it.

## Adding an email capture later

There's deliberately no form — a coming-soon page with an address on it is more
confident than one asking for a signup, and it can't break. If you want a list,
Buttondown or ConvertKit will give you an endpoint and it's about ten lines in
`index.html` under the contact line.
