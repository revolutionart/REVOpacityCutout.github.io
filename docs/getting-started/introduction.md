# Introduction

## Professional toolset for creating UVs in Blender

REVO Opacity Cutout converts opacity mask textures into real cutout mesh geometry directly inside Blender.

The add-on is designed for fast, repeatable foliage and card workflows where alpha-masked planes need clean geometry silhouettes.

## Main Features

- 2D / Planar Cutout mode for fast contour-based cutouts on flat cards
- 3D / Grid Mask mode for curved meshes where preserving surface flow matters
- 3D / Precise mode for high-accuracy cutouts on non-planar geometry
- One-click dependency installer from inside the panel
- Built-in quality presets for quick setup and consistent results
- Optional advanced controls for contour cleanup and triangulation behavior
- Integrated vertex painter tools for RGBA foliage channel workflows

## Default Shortcuts

No custom keyboard shortcuts are registered by default.

Use the N-Panel workflow:

- Open `3D View > N-Panel > REV OpacityCutout`
- Select mask image and channel
- Choose a quality preset
- Run one of the Generate actions

Tip: You can add your own keymaps in Blender Preferences if your team needs hotkeys.

### Main operators you will use

| Action | Shortcut | Notes |
| --- | --- | --- |
| Generate Cutout (2D / Planar) | None (button) | Main contour pipeline |
| Generate 3D Cutout (Grid Mask) | None (button) | Face-sampling mode on source mesh |
| Generate 3D Precise Cut | None (button) | UV clip + reprojection workflow |
| Install Dependencies | None (button) | Installs `opencv-python` and `pyclipper` |

## Required Blender version

- Minimum supported: Blender 4.2.0
- Add-on version: 1.0.0
- License: MIT

Dependency note:

- `opencv-python` and `pyclipper` are required
- Install them from the add-on panel with `Install Dependencies`
