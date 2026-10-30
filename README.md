# Galaxy-v2

**Genesis** is an interactive, space-themed visual experiment featuring an orbit-style 3D scene. The experience is contained in the top-level `index.html`.

## Preview locally

No package installation is required. Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. No deployment configuration is documented.

## Personalizing the experience

The page and its orbit scene are in `index.html`; use that file to locate the existing visible text and scene styling before changing them. The document links to Inter and Space Mono through Google Fonts. If you change the typeface, update both the font link and the corresponding font styling together; otherwise, keep the existing link intact.

The root file list contains no separate image or asset directory. If you add assets, place them intentionally and make the paths in `index.html` match their locations.

## Manual review checklist

These are review actions, not verified results.

- Open the known entry page, `index.html`, in a browser, or visit `http://localhost:8000` after starting the local server above.
- Try dragging to orbit the scene, scrolling to zoom, and double-tapping to reset the view. Check these controls with both pointer and touch input where available.
- Inspect the scene at a narrow phone-sized viewport and a wide desktop-sized viewport. Check that the controls remain usable and the scene remains visible.
- Check the Google Fonts link if typography was changed. If you added image or media assets, check that each reference in `index.html` matches its actual path.
