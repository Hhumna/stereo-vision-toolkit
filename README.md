# Stereo Vision Toolkit

Browser-based stereo reconstruction, depth mapping, ML-style segmentation, AR line overlays, and interactive 3D point-cloud visualization — all running directly in the browser.

## Overview

Stereo Vision Toolkit is a lightweight, single-page web application that demonstrates a complete stereo-vision workflow from image input to 3D reconstruction. The project is designed for experimentation, visualization, and educational use, allowing users to upload:

- two stereo images for reconstruction,
- a single image for segmentation and edge analysis, or
- a short panning video for frame-pair extraction.

The application runs entirely on the client side using browser technologies, making it easy to open locally or host as a static site.

## Features

- Stereo depth estimation using a classical correspondence pipeline
- Interactive AR-style line overlays derived from scene structure
- Unsupervised region segmentation for visual analysis
- Live 3D point-cloud rendering with orbit and zoom controls
- Built-in reference stereo pair and sample assets
- Zero backend dependency for the core experience

## Tech Stack

- HTML5
- CSS3
- JavaScript
- OpenCV.js
- three.js

## Project Structure

```text
stereo-vision-toolkit/
├── index.html              # Main application entry point
├── README.md               # Project documentation
└── Test-Samples/           # Reference sample images and video assets
```

## How It Works

The app follows a streamlined visual pipeline:

1. Load a stereo input or capture pair
2. Estimate disparity and produce a depth map
3. Generate segmentation and structural edge overlays
4. Reproject the disparity map into 3D space
5. Render the resulting point cloud interactively in the browser

## Local Development

Because this project is a static site, you do not need a build system or package installation.

### Run locally

From the project root:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deployment

This repository can be hosted as a static website on any standard static host.

### Recommended options

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages

For GitHub Pages, publish the root branch content directly from `main` as a static site.

## Usage Notes

- Use a stereo pair taken a few centimeters apart for best reconstruction quality.
- The reference benchmark pair helps validate the visual pipeline before using custom captures.
- All processing is browser-side, so performance depends on the device and input size.

## License

This project is provided for educational and experimental use.

## Repository Purpose

This repository showcases a browser-first approach to computer vision and interactive visualization, combining classical image-processing concepts with modern web rendering.
