# Human + Machine — 3D Anatomy Explorer
An interactive 3D human body and a **BMW R 1250 GS Adventure–inspired motorcycle**, side by side. Zoom in to separate the models and point at a component to learn its function.

Created with **Astra**. Arjun Reddy guided the idea, features, and feedback; Astra generated the code and procedural models.

## Features

- **195 labeled parts:** 125 human parts and 70 motorcycle components.
- Zoom-driven separation and reassembly.
- Hover descriptions and click-to-select highlighting.
- Human-only, motorcycle-only, and combined views.
- System filters and a component selector.
- Collapsible Explore controls below the model view.
- Offline browser viewer and downloadable GLB model.

## Open the viewer

1. Click **Code → Download ZIP** on this repository and extract it.
2. Open **Anatomy-Explorer.html** in desktop Chrome or another WebGL-capable browser.
3. Scroll to separate the models, drag to rotate, and hover to explore.

No installation, internet connection, or local server is required. WebGL must be available. Clicking the HTML file on GitHub displays its source; download it to run the viewer.

## Controls

| Action | Control |
| --- | --- |
| Separate or reassemble | Scroll or use the separation slider |
| Rotate | Drag on the canvas |
| Read a description | Hover over a component |
| Keep a selection | Click a component |
| Release a selection | Click empty canvas |
| Change model or system | Expand **Explore controls** |
| Find a component | Use the component dropdown |
| Restore the assembled view | **Reset view** |
| Download the GLB | **Save GLB** |
| Touch interaction | Drag, pinch, and tap |

## Project files

| File | Purpose |
| --- | --- |
| `Anatomy-Explorer.html` | Self-contained interactive viewer |
| `Human-and-Motorcycle.glb` | Combined 3D model with explosion animation |
| `components.json` | Component names, descriptions, and metadata |
| `source/` | Python generators and HTML viewer template |
| `README.txt` | Additional usage notes |

## Rebuild from source

Requires Python 3, with no third-party Python dependencies.

From the repository folder, run:

```bash
python source/add_motorcycle.py
python source/update_viewer.py
```

Generated files appear in `source/combined/`. Copy the updated viewer and model from there to the repository root if you want to publish a rebuilt version.

## GLB behavior

The GLB contains 195 named meshes and an **Explode and reassemble** animation. Compatible 3D viewers can play the animation. Automatic zoom separation, filtering, and hover descriptions are implemented in the supplied HTML viewer; generic GLB viewers do not automatically provide these interactions.

## Scope and limitations

This is a stylized educational prototype, not a complete medical atlas, official BMW CAD model, or repair guide. Anatomical shapes and counts are simplified. The motorcycle is inspired by the R 1250 GS Adventure, with simplified dimensions and mechanisms. The windscreen is rendered as opaque blue.

GLB structure, geometry bounds, JavaScript syntax, and control logic were checked during development. Control checks used mocked WebGL; live automated browser rendering was unavailable. Cross-browser and touch-device testing remain limited.
