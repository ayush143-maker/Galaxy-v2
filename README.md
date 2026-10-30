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

These are review actions, not verified results or measured performance.

- Open `index.html` in a browser, or visit `http://localhost:8000` after starting the local server above.
- Try dragging to orbit the scene, scrolling to zoom, and double-tapping to reset the view. Check these controls with both pointer and touch input where available.
- Inspect the scene at a narrow phone-sized viewport and a wide desktop-sized viewport. Check that the controls remain usable and the scene remains visible.
- Check local image, audio, and font references against files that exist at the referenced paths. The root file list contains no separate image or asset directory.
- Review any added media for appropriate dimensions and file size. Remove an asset only after confirming it is no longer referenced.
- The page links to Inter and Space Mono through Google Fonts. Confirm that this external font dependency is intentional and that both fonts are used; keep the link and font styling aligned if typography changes. Review any external script references you add in the same way, and avoid dependencies that are not needed.

## Accessibility review checklist

These are checks to perform after relevant changes, not verified results.

- Try to reach and use the orbit, zoom, and reset interactions using only a keyboard. If an interaction is available only by dragging, scrolling, or double-tapping, check whether an equivalent keyboard-operable control is available or needed.
- Check that keyboard focus is visible on each interactive control and distinguishable against the scene and page background.
- Review control names and instructions so they describe the action (such as orbit, zoom, or reset) rather than relying on an icon or gesture alone.
- Check contrast for the page text, instructions, and control labels against their backgrounds.
- If the 3D scene conveys information beyond decoration, consider whether a concise text alternative or description is needed; check alternatives for any images added to the page.
- Check the scene and any related transitions with reduced motion requested. Consider a less animated presentation for nonessential movement.