---
title: Space Engineers Utilities
---

<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
If the options in this section are **greyed out**, that is because the currently active material is **linked into** the `BLEND`-file - for example from a MatLib. As such, unless the material is made local, it cannot be edited directly.
</div></div>

![](/modding-reference/assets/images/reference/seut/shader-editor-panel_1.png)

### PaintedMetal_Colorable
This line displays the name of the currently active material as well as a small preview of how it looks.

### Override MatLib
This checkbox allows you to force a custom material created in the current file to **overwrite a material** with the same name that is linked into this `BLEND`-file. Normally, if a material with name X in a file also exists in a MatLib, the local material would be replaced by the MatLib material X. This ensures that the *local* material X is used over the one contained in a MatLib. Refer to the [*&nbsp;*{: .fa .fa-map}Override Vanilla Material Tutorial]() for more details.

### Technique
This dropdown defines the way Space Engineers **renders the material**. Valid techniques are:

* **MESH** - The standard technique.
* **DECAL** - Makes the material look like it's part of the model behind it.
* **DECAL_NOPREMULT** - Higher accuracy of transparency than 'DECAL', but same visual style.
* **DECAL_CUTOUT** - Makes the material look like it cuts into the model behind it.
* **GLASS** - Transparent material - requires additional values to be set in `TransparentMaterials.sbc`.
* **ALPHA_MASKED** - Has an alphamask texture.
* **SHIELD** - Animated material used on SafeZone shield - currently limited to default one.
* **HOLO** - Transparent LCD screen texture.
* **FOLIAGE** - Used for half-transparent textures like leaves - shadows observe transparency in texture.

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Using the Technique `SHIELD` on a material applied to a block of certain types might cause Space Engineers to crash.
</div></div>

### Facing
This setting affects the way a **material is displayed** in Space Engineers. Currently it is **unclear what exactly these settings affect** but it is likely this is connected to a material being always rotated to face the camera. Valid options are:

* **None** - This is the normal Facing setting. This is what is set for all vanilla materials.
* **Vertical** - Vertical facing mode.
* **Full** - Full facing mode.
* **Imposter** - Imposter facing mode.

### Wind Scale
This value is mainly relevant for tree and bush materials. It is **unclear what exactly the effect of this value is** ingame but it relates to the degree to which objects with this material move in the wind.

### Wind Frequency
This value is mainly relevant for tree and bush materials. It is **unclear what exactly the effect of this value is** ingame but it relates to the degree to which objects with this material move in the wind.

### Create Material
Clicking this button creates a new material on the selected object. Refer to the [*&nbsp;*{: .fa .fa-map}Material Creation Tutorial](/modding-reference/tutorials/tools/3d-modelling/seut/create-material) for more details.

### import Material
Clicking this button allows you to select a `Material Library`-type XML file and import the materials defined within into the current BLEND file.
<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>
