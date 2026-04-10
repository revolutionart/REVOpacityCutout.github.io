## General

### Q: Can I paint multiple objects at once?
Yes, select all objects before applying; most operators loop over all selected meshes
### Q: Will reloading the addon lose my painted data?
No, vertex color data lives on the mesh, not the addon
### Q: Live Editing is slow on my mesh
Turn it off and use Apply manually; high-poly meshes are expensive to re-evaluate on every slider drag
### Q: Is there a hard mesh size or polygon limit?
No, there is no hard built-in limit. The practical limit is set by the user’s hardware, so very large meshes can still work, but performance will vary depending on the computer. The add-on has been confirmed to work with models ranging from a plane mesh to 8 million polygons.

## Setup

### Q: What layer name should I use?
Whatever you'd like, by default its set to FoliageVertexPaint.

---
## Painting

### Q: Why did my other channels go black when I painted?
You filled ALL channels. Use the channel lock or Override only the one you need
### Q: I painted Red but the viewport looks wrong
Switch preview to R channel using the channel buttons, or hit Flat/See Vertex Color first
### Q: My gradient looks blocky/jagged
Increase Smooth Iters, or lower Falloff
### Q: Stem→Leaf painted the wrong direction
Toggle Reverse, or re-select the base/root verts before applying 

---
## Per-Plant tools

### Q: Select Nearby isn't grouping my leaves with the stem
Enable Detect Overlap, or increase Group Distance slightly
### Q: Apply Random gives the same value each time for Green
It doesn't; it re-seeds from system time every click. If values look similar, widen Min/Max range
### Q: Blue channel keeps giving similar colors
The 35% contrast gap logic helps but works best with a wide Min/Max range (e.g. 0–1)

---
## Cutout

### Q: Even Triangles looks wrong, What now?
Try the following in the advanced settings.

- **Contour Tolerance**: lower values keep the traced silhouette tighter and often fix unstable edge shapes.

- **Gap Closing Radius**: increase it when tiny slits or breaks should merge; leave it at `0` to use the preset default instead of forcing a tiny manual override.
- **Quality Preset**: move from **Medium** to **High** when thin features need a cleaner contour before re-triangulation.

Make sure to always cut again after changing the advanced values, this is important, after that re-try **Apply Even Triangles**

First undo the Even Triangles and the cutout. Adjust the advanced settings, then click Generate Cutout and Apply Even Triangles to generate the new result.