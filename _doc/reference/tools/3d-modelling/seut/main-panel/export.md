---
title: Export
---
![](/modding-reference/assets/images/reference/seut/export_1.png)

### Export All Scenes
This button will iterate through all scenes and their collections within the `BLEND`-file and export them one by one. 

### Export Current Scene
Exports all collections within the current scene.

### Delete Temp Files
By default, the only files resulting from export are the `SBC` and `MWM` files, as all **intermediary files are automatically cleaned up**. Untoggling this option will prevent these temporary files from being cleaned up and thus allows for debugging.

### SBC
This toggle controls whether a `SBC` file is generated on export. It is enabled by default but once the initial `SBC` has been adjusted, a new export is usually not needed.

### Large
This toggle controls whether the current scene is exported to large grid.

### Small
This toggle controls whether the current scene is exported to small grid.

### Rescale Factor
The rescale factor allows for the rescaling of the exported models. A large grid block can be exported as a small grid block by setting this value to `0.2`.

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Don't forget to change your SubtypeId before exporting a small grid version of your block or it will overwrite your previously exported large grid version.
</div></div>

### Export Folder
The directory to export your model to. Must contain `Models\` in its path to be eligible. Set this to directly export into your mod's directory.

#### Copy Export Folder
This button copies the current `Export Folder` to all other scenes within the `BLEND`-file.
<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>