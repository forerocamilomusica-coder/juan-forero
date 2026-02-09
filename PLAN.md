# AR Business Card Implementation Plan

## Goal Description
Create a web-based Augmented Reality business card using A-Frame and AR.js that can be viewed on a mobile device.

## Proposed Changes

### Project Structure
- `index.html`: Main AR scene.
- `assets/`: Directory for images (textures, profile pics).
- **[NEW] 3D Model**: `12221_Cat_v1_l3.obj` and `12221_Cat_v1_l3.mtl`.
- **[NEW] Custom Font**: `From Cartoon Blocks.ttf` -> MSDF format.

### Base Code Implementation
- Create `index.html` with the provided snippet.

### Design Enhancements
- **Name**: Juan Camilo Forero
- **Title**: Diseñador Industrial
    - **Font**: User requested "standard A-frame 3D type".
    - **Action**: Implement `aframe-text-geometry-component` (Extruded 3D text).
    - **Font Source**: Use a hosted standard typeface (e.g., `optimer_bold.typeface.json` or `helvetiker`).
    - **Color**: White (Material).
- **3D Model**: Integrate `12221_Cat_v1_l3.obj`.
- **Card Layout**:
    - [REMOVED] Plane background (dark).
    - Model positioned above text or to the side.
    - Text: Name and Title.

## Verification Plan
### Manual Verification
- Run a local server to avoid CORS issues.
- **[DEBUG]** Verify the 3D model loads. if not:
    - Check console for errors.
    - Verify `.mtl` texture paths (`Cat_diffuse.jpg`, `Cat_bump.jpg`).
    - Adjust scale (try larger/smaller).
    - Ensure lighting is sufficient.
- **Verify Font**: Check if text is extruded (3D) and legible.

## Deployment
- **GitHub**: Push code to a repository.
- **GitHub Pages**: Enable static hosting for the AR card.
