# Analog Film Studio

A small browser-based photo editor that gives digital images the character of classic color film. Choose a film stock, adjust the look, compare the original with the developed print, and download the result.

Photos are processed in the browser and are not uploaded. Saved looks are kept in this browser's local storage. The page loads its display fonts from Google Fonts; if those fonts are unavailable, it falls back to system fonts.

## Features

- Film looks inspired by Kodak Gold 200, Kodak Portra 400, Kodak Ektar 100, CineStill 800T, and Fuji Superia 400
- Natural, vibrant, muted, and vintage starting presets
- Controls for exposure, warmth, contrast, faded blacks, saturation, halation, light leaks, grain, dust, and vignette
- A draggable before-and-after comparison slider and a separate grain-size control
- Center crops for square, portrait, classic 3:2, and widescreen prints
- Save, apply, and delete custom looks in browser storage
- Optional 35mm frame and camera date stamp, prefilled from EXIF capture metadata when available
- Drag and drop or browse for multiple images, then switch between them in a contact sheet
- Export the current photo or whole roll as JPEG or lossless PNG; adjust JPEG quality and optionally develop at full resolution
- Responsive layout for desktop and mobile

## Use the site

Open the deployed site, drop in a photo or choose one from your device, then select a stock or preset. Drag the comparison slider to inspect the before and after. Choose a centered crop, adjust the look, and download as JPEG or PNG. Saved looks are available again in the same browser. Enable **Full-resolution export** to develop the original image dimensions instead of the smaller editing preview.

## Run locally

There is no build step or package installation. From the repository directory, start a local static server:

```sh
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a browser. You can also open `index.html` directly, though serving it locally is closer to how the deployed site runs.

## Project structure

```text
.
├── index.html   # Complete app: markup, styles, and image-processing code
└── README.md
```

The site is a static GitHub Pages project. Changes pushed to the configured branch are published by GitHub Pages; no build tool or backend is required.
