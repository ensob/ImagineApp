Title: fix: background-clip compatibility and minor UI fixes

Description:

- Adds `background-clip: text;` to `imaginative_art_generator.html` to improve cross-browser compatibility for gradient-filled headings.
- Updates the site title and header in `index.html` to "Imagine" and the Spanish tagline "Imagina lo que no puedes crear...hasta ahora...!".
- Ensures `digital_art_generator.html` has save/pause wiring and initializes particles and the `ArtGenerator` on load.

Testing steps:

1. From the repo root run a local static server:

```powershell
python -m http.server 8000
```

2. Open in your browser:

- http://localhost:8000/index.html
- http://localhost:8000/imaginative_art_generator.html
- http://localhost:8000/digital_art_generator.html

3. Verify:

- Canvas animates on the art pages.
- Clicking `Save Artwork` downloads a PNG (uses `canvas.toDataURL`).
- `Pause` stops the animation loop.

Notes:

- This repository contains single-file demos; no build step required. Use a static file server for local testing.
- If the remote default branch is not `main`, change the PR base branch in the UI when creating the PR.
