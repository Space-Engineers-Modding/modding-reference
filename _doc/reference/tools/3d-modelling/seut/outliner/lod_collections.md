---
title: Levels of Detail
---

These collections (LOD1, LOD2, LOD3) store the so called 'Levels of Detail' or 'LOD' versions of your model, these are extremely important to make use of, as GPU's only have so much VRAM available. 

The following is a good starting guide for what kind of detail you should put into each collection:

* **LOD1** - Might as well be just as good as the high quality version of the model, minus a few decals. This LOD level also replaces the `Main` mesh on the "Medium" model quality setting.
* **LOD2** - Remove decals, simplify tubes, spheres, etc. Investigate the usage of the `Decimate` modifier in blender.
* **LOD3** - Very low quality, spheres, tubes, etc can be extremely simplified at this range, and `Decimate` further

<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
In some cases, LOD models may override the main model by default. Here are the rules:
* **Extreme** - Forces the LOD system to disable entirely, planets and models will ignore LODs
* **High** - LOD system accounts for all models at their set LOD distances.
* **Medium** - The model in the `Main` collection is excluded from showing, LOD1 becomes the main model and LOD2 and LOD3 activate somewhat sooner
* **Low** - Same as Medium, but the distances in LOD level changes are reduced even further
</div></div>

<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>