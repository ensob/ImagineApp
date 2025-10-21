<!--
Use this template to describe the change when opening a Pull Request.
-->

# Summary

fix: background-clip compatibility and minor UI fixes

## What this does

- Adds `background-clip: text;` for better cross-browser compatibility in `imaginative_art_generator.html`.
- Updates the site title and header in `index.html` to "Imagine" / "Imagina lo que no puedes crear...hasta ahora...!".
- Minor wiring and UI improvements in `digital_art_generator.html` (save/pause handlers, init).

## How to test

1. From the repo root run a simple static server, e.g.:

```powershell
python -m http.server 8000
```

2. Open the pages in your browser:

- http://localhost:8000/index.html
- http://localhost:8000/imaginative_art_generator.html
- http://localhost:8000/digital_art_generator.html

3. Verify:
- Canvas animates.
- `Save Artwork` downloads a PNG (via `canvas.toDataURL`).
- `Pause` stops the animation.

## Notes
- This is a small, client-side demo — no build or server required beyond a static file server.
