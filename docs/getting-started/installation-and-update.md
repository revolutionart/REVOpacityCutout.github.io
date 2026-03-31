# Installation and Update

## Installation

1. Open Blender.
2. Go to `Edit > Preferences > Add-ons`.
3. Select `Install...` and choose the `opacity_cutout_addon` package.
4. Enable `REVO Opacity Cutout` in the add-ons list.
5. Open `3D View > N-Panel > REV OpacityCutout`.
6. Click `Install Dependencies` to install required Python packages.

Required dependencies:

- `opencv-python`
- `pyclipper`

## Update

1. Disable the previous version in Blender add-ons.
2. Install the updated plugin package.
3. Re-enable the add-on.
4. Restart Blender if required.

## Verify installation

- Confirm the `REV OpacityCutout` tab appears in the 3D View N-Panel.
- Confirm `Install Dependencies` completes without errors.
- Confirm you can run a first test with `2D / Planar Cutout` on a simple masked plane.

## First-run sanity check

1. Create or select a mesh card with valid UVs.
2. Assign a material with an opacity image.
3. In the panel, choose the mask image (or use auto-detect).
4. Select a quality preset.
5. Click `Generate Cutout` in `2D / Planar Cutout`.
6. Verify generated geometry follows the opacity silhouette.
