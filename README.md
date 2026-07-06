# こえむすび — asset host

Static files for the **こえむすび (koemusubi)** Second Life kana-TTS HUD. Hosted on
GitHub Pages (Fastly-backed, `access-control-allow-origin: *`) so the in-world
Media-on-a-Prim browser can load them — GitHub Pages avoids the Cloudflare bot
mitigation that intermittently 403s SL's CEF on public CDNs like jsDelivr.

- `build/kuromoji.js` — the [kuromoji.js](https://github.com/takuyaa/kuromoji.js)
  Japanese morphological analyzer (© takuyaa, Apache-2.0).
- `dict/*.dat.gz` — its IPADIC dictionary.
- `hud1.png` — the HUD panel art.
- `index.html` — a live self-test (type Japanese, see the reading).

The HUD's reader script points `CDN_BASE` here. To update kuromoji, replace the
files and push; the Pages URL is stable.
