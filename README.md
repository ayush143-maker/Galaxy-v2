# Galaxy-v2

**Genesis** is an interactive, space-themed visual experiment featuring an orbit-style 3D scene. The experience is contained in the top-level `index.html`.

## Preview locally

No package installation is required. Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit http://localhost:8000. No deployment configuration is documented.

## Personalizing the experience

The page and its orbit scene are in `index.html`; use that file to locate the existing visible text and scene styling before changing them. The document links to Inter and Space Mono through Google Fonts. If you change the typeface, update both the font link and the corresponding font styling together.

The root file list contains no separate image or asset directory. If you add assets, place them intentionally and make the paths in `index.html` match their locations.

## Troubleshooting

Use these as diagnostic steps, not as claims that the page currently has a problem:

1. **Confirm the entry page.** Open the top-level `index.html`, or serve the repository directory and visit its root URL. Confirm the server is serving this project if the expected scene does not appear.
2. **Check paths and local files.** Preserve relative paths when moving the page or adding assets. If a local asset request fails, confirm the file exists and that its reference in `index.html` matches its location. No separate image or asset directory is listed at the repository root.
3. **Inspect browser diagnostics.** Check the console for errors on load and while using the scene. In the Network panel, inspect failed requests and their URLs to help identify local path or loading problems.
4. **Separate network-dependent resources.** The page links Inter and Space Mono from Google Fonts. Those font requests require network access to the external service; they are distinct from local assets. If font requests fail, consider whether the page's fallback typography remains legible. Confirm any additional remote requests are intentional.

## Configuration and data handling

This repository contains a static `index.html`; no environment template or backend configuration is listed. Do not place credentials or private values in the page or other tracked files. Static-page values are sent to the browser and are not secret. Review page content and any assets you add before sharing or publishing them. The page links to Google Fonts, so visitors' browsers may also request those fonts from that external service.

## Browser and layout review checklist

This is a checklist for future review, not a report of completed compatibility testing or verified results.

- Review the page in current versions of browsers relevant to the experience's intended audience.
- Try dragging to orbit the scene, scrolling to zoom, and double-tapping to reset the view. Where available, try both pointer and touch input; do not assume one input mode verifies the other.
- Inspect the scene at a narrow phone-sized viewport and a wide desktop-sized viewport. Check that the scene remains visible and controls remain usable without clipping or unwanted overflow.
- Review the dimensions and file sizes of media you add. Remove an asset only after confirming it is no longer referenced.

## Accessibility review checklist

These are future checks, not verified results.

- Try to reach and use the orbit, zoom, and reset interactions using only a keyboard. If an interaction is available only by dragging, scrolling, or double-tapping, consider whether an equivalent keyboard-operable control is needed.
- Check that keyboard focus is visible on each interactive control and distinguishable against the scene and page background.
- Review control names and instructions so they describe the action, such as orbit, zoom, or reset, rather than relying on an icon or gesture alone.
- Check contrast for page text, instructions, and control labels against their backgrounds.
- If the 3D scene conveys information beyond decoration, consider whether a concise text description is needed; check alternatives for any images added to the page.
- Check the scene and related transitions with reduced motion requested. Consider a less animated presentation for nonessential movement.