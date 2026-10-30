# Galaxy-v2

**Genesis** is a procedural space-scene experiment that moves from a cinematic camera sequence into an interactive orbit view. The scene is rendered with Three.js and WebGL in the top-level `index.html`; stars and nebulae are generated in code rather than loaded as image assets.

## Preview locally

No package installation is required. Open `index.html` in a browser, or serve the repository directory:

```sh
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000). A browser with WebGL support is needed for the Three.js scene. There is no documented build step or deployment configuration.

## Experience and controls

A timed loading bar precedes a cinematic sequence of 20 camera shots, followed by the orbit view. The bar advances by timed random increments; it is not a measurement of scene or asset loading. Select **Skip** to move directly from the cinematic to interactive mode. Drag with one pointer to orbit, use the mouse wheel or a two-pointer pinch to zoom, and double-tap on touch to return the orbit camera to its preset values. After three seconds without orbit input, the interactive camera gradually rotates on its own.

The HUD shows distance and time values, while a progress rail tracks the cinematic and reaches 100% in interactive mode. There is an important control mismatch: after entering interactive mode, the button is labeled **Reset**, but its click handler calls the transition function that immediately returns in that mode. It does not reset the scene. The touch double-tap reset remains available.

## Rendering and resources

The procedural scene contains 140,000 galaxy points, two nebula point clouds, a 16,000-point companion, and a 30,000-point starfield. It uses an EffectComposer render pass and UnrealBloomPass post-processing. These point counts and effects can be demanding on some devices; rendering performance depends on the visitor’s browser and hardware.

Three.js 0.160.0 and its post-processing modules load from unpkg through an import map. Inter and Space Mono load from Google Fonts. These CDN-hosted libraries and fonts require network access. The page makes no external API requests and does not save scene state or user settings in local storage. Edit the scene and styles in `index.html`; the repository root lists no separate image or asset directory.