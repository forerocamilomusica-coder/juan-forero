# AR Business Card Walkthrough

## Overview
We have successfully created an Augmented Reality business card using A-Frame and AR.js. The card features a 3D model, 3D text (extruded), and no background, allowing it to blend with the real world.

## Features Implemented
- **Base AR Scene**: Uses `hiro` marker detection.
- **3D Model**: Integrated `12221_Cat_v1_l3.obj` (Cat model).
- **3D Text**: Utilized `aframe-text-geometry-component` with `optimerBold` font for the name ("Juan Camilo Forero") and title ("Diseñador Industrial").
- **Design**: Removed the plane background for a holographic effect.

## How to View
1.  **Open the Link**: Go to your GitHub Pages URL (e.g., `https://forerocamilomusica-coder.github.io/juan-forero/`).
2.  **Allow Camera**: Grant camera permissions when asked.
3.  **Point Camera**: Aim your phone's camera at the [HIRO marker](https://upload.wikimedia.org/wikipedia/commons/4/48/Hiro_marker_ARjs.png).

## Files Created
- `index.html`: Main AR application code.
- `assets/`: Contains 3D model files (`.obj`, `.mtl`, textures).
- `custom-font.*`: (Optional/Previous) MSDF font files (preserved in repo).
