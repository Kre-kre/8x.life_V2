# 8x.life — homepage redesign

Static site. No build step. Works on desktop and mobile.

## Host on GitHub Pages
1. Create a repo and push the contents of this folder to its root (keep the folder structure).
2. Settings → Pages → Source: "Deploy from a branch" → branch `main`, folder `/ (root)`.
3. The site is live at `https://<user>.github.io/<repo>/`. `.nojekyll` is included so Pages serves every file as-is.

Any other static host (Vercel, Netlify, S3, Cloudflare Pages) works the same: point it at this folder.

## Files
- `index.html` — the page (markup + logic in one file).
- `8x-content.js` — ALL replaceable content: manifesto lines, founders, media captions, the four products + talent links, traits, rules. Edit this, not the components.
- `image-slots.state.json` — photos dropped into the page (founder portraits, carousel stills). Replace by dropping new images in the editor, or point the slots at files in `assets/`.
- `assets/` — vector grain textures (`grain-fade.svg`, `grain-sweep.svg`) and the gold frame.
- `image-slot.js` — photo drop-zone component. `support.js` — runtime.

## Links
- Join the platform → https://8x.careers
- Join the network → each world card opens its talent-side page (set in `8x-content.js` → `worlds[].talent`).

## Fonts
Google Fonts (Instrument Sans, Instrument Serif, IBM Plex Mono). Self-host them in `assets/fonts/` if you need fully offline.
