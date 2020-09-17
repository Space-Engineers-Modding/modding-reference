---
title: Levels of Detail
---

These collections (LOD1, LOD2, LOD3) store the so called 'Levels of Detail' or 'LOD' versions of your model.

These are extremely important to make use of, as GPU's only have so much VRAM available. 

The following is a good starting guide for what kind of detail you should put into each collection:
<br><br/>

* **LOD1** - Might as well be just as good as the high quality version of the model, minus a few decals. This LOD level also replaces the `Main` mesh on the "Medium" model quality setting.
* **LOD2** - Remove decals, simplify tubes, spheres, etc. Investigate the usage of the `Decimate` modifier in blender.
* **LOD3** - Very low quality, spheres, tubes, etc can be extremely simplified at this range, and `Decimate` further


<br><br/>