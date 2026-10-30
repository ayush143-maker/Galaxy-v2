# Galaxy-v2

**Genesis** is an interactive, space-themed visual experiment featuring an orbit-style 3D scene. The experience is contained in the top-level `index.html`.

## Preview locally

No package installation is required. Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. No deployment configuration is documented.

## Editing the experience

The page, scene, and styling are in `index.html`. The document links to Inter and Space Mono through Google Fonts. If you change typefaces, keep the font link and the corresponding font styling in sync. The repository root lists no separate image or asset directory; if you add assets, make their paths in `index.html` match their locations.

The page's font requests depend on network access to Google Fonts. If those requests are unavailable, check that the fallback typography remains legible.

## Contributor handoff

Keep changes scoped to the relevant scene, text, or styling in `index.html`. Preserve the filename and existing references unless a change requires updating them; when moving or adding an asset or changing a font, update the corresponding reference as well. In the handoff, summarize what changed and identify the affected page area or file.

Before publishing, manually review the scene in a browser at narrow phone-sized and wide desktop-sized viewports. Try the existing orbit, zoom, and reset interactions, using pointer and touch input where available. This is a review checklist, not a report of completed compatibility testing or verified results.
