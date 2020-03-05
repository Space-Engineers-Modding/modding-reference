---
title: Space Engineers Utilities
---

<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
If the options in this section are **greyed out**, that is because the currently active material is **linked into** the `BLEND`-file - for example from a MatLib. As such, unless the material is made local, it cannot be edited directly.
</div></div>

![](/modding-reference/assets/images/reference/seut/node-editor-panel_1.png)

### PaintedMetal_Colorable
This line displays the name of the currently active material as well as a small preview of how it looks.

### Preset: No Alpha, No Emissive
This line displays the material preset that was used to create the material. The preset determines which texture-types the material supports and how they are displayed.

### Override MatLib
This checkbox allows you to force a custom material created in the current file to **overwrite a material** with the same name that is linked into this `BLEND`-file. Normally, if a material with name X in a file also exists in a MatLib, the local material would be replaced by the MatLib material X. This ensures that the *local* material X is used over the one contained in a MatLib. Refer to the [*&nbsp;*{: .fa .fa-map}Override Vanilla Material Tutorial]() for more details.

### Technique
This dropdown defines the way Space Engineers **renders the material**. Valid techniques are:

* **MESH** - The standard technique.
* **DECAL** - Makes the material look like it's part of the model behind it.
* **DECAL_NOPREMULT** - Higher accuracy of transparency than 'DECAL', but same visual style.
* **DECAL_CUTOUT** - Makes the material look like it cuts into the model behind it.
* **GLASS** - Transparent material - requires additional values to be set.
* **ALPHA_MASKED** - Has an alphamask texture.
* **SHIELD** - Animated material used on SafeZone shield - currently limited to default one.
* **HOLO** - Transparent LCD screen texture.

### Facing

### Wind Scale

### Wind Frequency

### Preset

### Create Material


<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>
