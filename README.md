# Galaxy-v2

**Genesis** is an interactive, space-themed visual experiment featuring an orbit-style 3D scene. The experience is contained in the top-level `index.html`.

## Preview locally

No package installation is required. Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000). No deployment configuration or build step is documented.

## Editing the experience

The page, scene, and styling are in `index.html`. The page links to Inter and Space Mono through Google Fonts. If changing typefaces, keep the font link and corresponding styling in sync. These font requests depend on network access; check that fallback typography remains legible when they are unavailable.

The repository root lists no separate image or asset directory. If adding assets, make their paths in `index.html` match their locations. For a static publication, serve the repository root and include the page and any referenced assets.

## Scene controls and review

The experience includes orbit, zoom, and reset interactions. After editing, try these controls in a browser, using pointer and touch input where available. Review the scene at narrow phone-sized and wide desktop-sized viewports.

## Repository map

- `index.html` — page entry point, scene, styling, and font references.

No package installation, build command, or deployment settings are documented for this static page.