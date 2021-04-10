---
title: Import
---
![](/modding-reference/assets/images/reference/seut/import_1.png)

### Import FBX
This button allows for the import of `FBX` files. Imported geometry is **automatically processed further**, thus it is heavily recommended to use this button over the default Blender `FBX` import option.

### Complete Import
This button allows you to select a target `FBX` file and then attempts to also import all associated models into the scene and sort it into the collections - LODs, BS, BS_LODs as well as the main model.

### Fix Scratched Materials
SDK models have a scratched texture mapped to their bevels by default - but it does not appear ingame because it is replaced on MWM conversion. That method does not work for SEUT. 
This option (active by default) will replace these materials with their non-scratched counterparts automatically on import.

### Remap Materials
This button replaces all materials in the `BLEND`-file with the materials in the linked MatLibs, if they have common names.

### Convert to New Structure
This button should be used first thing when opening `BLEND`-files that have been set up with the old 2.7x (Harag or Balmung's) Blender plugin. It will convert the old file structure to the new structure used within SEUT.

### Attempt to Fix Positioning
This button attempts to fix the positioning of an imported `FBX` object as well as its child objects as some of the vanilla `FBX` files, on import, can be misaligned due to issues in Blender's FBX import code.

### Make Blender compatible
This button converts the names of bones in the `BLEND`-file to a Blender-compatible format.

### Make SE compatible
This button converts the names of bones in the `BLEND`-file to a Space Engineers-compatible format.
<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>