---
title: SEUT Error Codes
---

### E001
```
SEUT: Import error. Imported object not found.
```
**Cause**

After import, the imported objects could not be found.

**Solution**

There is no real way to solve this issue beyond attempting another import. It's likely that the `FBX`-file is corrupted in some way.

### E002
```
SEUT: Collection {variable_1} not found, excluded from view layer or empty. Action not possible.
```
**Cause**

For the action that was attempted, the listed collection must be available and it was not due to either not existing, being empty, or being excluded from the view layer.

**Solution**

* If the specified collection does not exist, hit the `Recreate Collections`-button in the [*&nbsp;*{: .fa .fa-database}SEUT Main Panel](/modding-reference/reference/tools/3d-modelling/seut/main-panel#recreate-collections).
* If the specified collection is empty, place at least one object into the collection.
* If the collection is excluded from the view layer, be sure to tick its checkbox in the outliner:
  
  ![](/modding-reference/assets/images/tools/seut/troubleshooting_E002.png)

### E003
```
SEUT: {variable_1} path '{variable_2}' doesn't exist.
```
**Cause**

The folder or file specified in the given path does not exist.

**Solution**

Re-enter the path in the respective field, preferrably by using the file browser.

![](/modding-reference/assets/images/tools/seut/troubleshooting_E003.png)

*(The above is an example of the `Export Path` file browser, but this error may refer to another path.)*

### E004
```
SEUT: No SubtypeId set for scene '{variable_1}'.
```
**Cause**

No `SubtypeId` has been set for the specified scene. 

**Solution**

This should never happen anymore but if it still does, simply specify a `SubtypeId` in the [*&nbsp;*{: .fa .fa-database}SEUT Main Panel](/modding-reference/reference/tools/3d-modelling/seut/main-panel#subtypeid).

### E005
```
SEUT: Linking to scene '{variable_1}' from '{variable_2}' would create a subpart instancing loop.
```
**Cause**

Linking the current scene to the selected other scene would create a circle of reference and thus an infinite loop.

**Solution**

Check all your scenes and ensure that all `subpart empties` point to the correct target scenes. A reference loop should never be needed to set up a model correctly.

### E006
```
SEUT: LOD2 cannot be set if LOD1 is not or LOD3 if LOD2 is not.
```
**Cause**

A "lower" LOD collection is empty or doesn't exist while a "higher" one exists and / or contains objects. 

**Solution**

It is not possible & does not make sense to have higher LOD collections without the lower ones. Move the contents of the higher ones down to the lower ones so instead of, for example, having `LOD1` empty and objects in `LOD2`, move those objects into the `LOD1`-collection.

### E007
```
SEUT: '{variable_1}' texture filepath in local material '{variable_2}' does not contain 'Textures\\'. Cannot be transformed into relative path.
```
**Cause**

The path to the specified texture of the listed local (non-MatLib) material does not contain the component `Textures\\`. 

**Solution**

Place the textures in the specified image node of the material into a folder named `Textures`. They can also be in a subfolder *within* the folder `Textures`. You will have to place the `DDS`-versions of those textures within the same folders (starting from `Textures`) in your mod.

### E008
```
SEUT: BLEND file must be saved before export.
```
**Cause**

The attempted action requires the `BLEND`-file to have been saved.

**Solution**

Save your `BLEND`-file.

### E009
```
SEUT: Cannot create empties for more than one object at a time.
```
**Cause**

More than one object is selected when attempting to create a `highlight empty`

**Solution**

Only select a single object when trying to create a `highlight empty`.

### E010
```
SEUT: Cannot run Simple Navigation if no SEUT collections are present.
```
**Cause**

Simple Navigation only works on SEUT collections. There are no SEUT collections in the current scene.

**Solution**

Press the `Recreate Collections`-button in the [*&nbsp;*{: .fa .fa-database}SEUT Main Panel](/modding-reference/reference/tools/3d-modelling/seut/main-panel#recreate-collections) to create the SEUT collections.

### E011
```
SEUT: Invalid LOD distances. LOD2 cannot be set to be displayed before LOD1 or LOD3 before LOD2.
```
**Cause**

A "lower" LOD collection's distance is set to further than a "higher" LOD collection.

**Solution**

Change the LOD collection distances so that the distances of "higher" LOD collections are always further than that of the next "lower" LOD collection. For example, the distance for `LOD2` cannot be 25m if the distance for `LOD1` is 50m. It must be greater than 50m.

### E012
```
SEUT: Path to {variable_1} (Addon Preferences) '{variable_2}' not valid.
```
**Cause**

The path selected in the specified field in the addon's preferences is not valid.

**Solution**

Use the file browser to set a new path that points to the correct location.

### E013
```
SEUT: Path to {variable_1} (Addon Preferences) not valid - wrong target file: Expected '{variable_2}' but is set to '{variable_3}'.
```
**Cause**

The wrong target file has been selected for the specified tool in the addon's preferences.

**Solution**

* Use the file browser to select the correct tool's `EXE`-file.
* If this error appears when attempting to set the `Havok Filter Manager` filepath, ensure that you have *installed* Havok, and are not attempting to select the Havok installation `EXE`-file.

### E014
```
SEUT: Export path '{variable_1}' in scene '{variable_2}' does not contain 'Models\\'. Cannot be transformed into relative path.
```
**Cause**

The `Export Folder` set for the specified scene does not point to a directory within a folder named `Models`.

**Solution**

Set the `Export Folder` for the specified scene to a folder named `Models`. It also point to a subfolder *within* the folder `Models`.

### E015
```
SEUT: Invalid {variable_1} setup. Cannot have {variable_1}2 but no {variable_1}1 or {variable_1}3 but no {variable_1}2.
```
**Cause**

Either the LOD or Build Stage collections are set up in an invalid manner.

**Solution**

It is not possible & does not make sense to have higher LOD / BS collections without the lower ones. Move the contents of the higher ones down to the lower ones so instead of, for example, having `LOD1` / `BS1`empty and objects in `LOD2` / `BS2`, move those objects into the `LOD1` / `BS1`-collection.

### E016
```
SEUT: Scene '{variable_1}' could not be exported.
```
**Cause**

There was an error when attempting to export the specified scene.

**Solution**

View the errors that are listed to have happened during export and resolve them, then attempt to export again. If no errors are listed, refer to the `Blender System Console` for more detailed error output.

![](/modding-reference/assets/images/tools/seut/troubleshooting_E016.png)

### E017
```
SEUT: An error has occurred in the FBX exporter. Try exiting Edit-Mode before exporting.
```
**Cause**

An unspecified error has occurred during export to `FBX`.

**Solution**

This error can have various causes but the most common one is due to not being in `OBJECT`-mode within your Viewport when starting the export.

![](/modding-reference/assets/images/tools/seut/troubleshooting_E017.png)

### E018
```
SEUT: Cannot set SubtypeId to a SubtypeId that has already been used for another scene in the same BLEND file.
```
**Cause**

The `SubtypeId` that has been entered is already in use for a different scene in this `BLEND`-file.

**Solution**

Two scenes cannot have the same `SubtypeId`. There is no way around this - one of the two scenes will have to be named differently.

### E019
```
SEUT: No export folder defined for scene '{variable_1}'.
```
**Cause**

No `Export Folder` has been defined for the specified scene.

**Solution**

Define an `Export Folder` for the specified scene.

![](/modding-reference/assets/images/tools/seut/troubleshooting_E019.png)

### E020
```
SEUT: Deletion of temporary files failed.
```
**Cause**

An unspecified error occurred during deletion of the temporary files. (The files used to build the `MWM`-file from.)

**Solution**

This error can have various causes. Attempt the following:
* Check any `.log` files placed in your `Export Folder` for errors.
* Ensure that you have the latest & correct version of the `MWMBuilder`.

### E021
```
SEUT: Available MatLibs could not be refreshed.
```
**Cause**

There was an unspecified error when attempting to refresh the available MatLibs.

**Solution**

The common cause for this is that the paths set in SEUT's addon preferences have been reset and are currently empty.

### E022
```
SEUT: Too many objects in '{variable_1}'-collection. Collection contains {variable_2} but Space Engineers only supports a maximum of 16.
```
**Cause**

There are too many separate objects in the specified collection.

**Solution**

Reduce the amount of objects in the specified collection. Note that instead making the existing objects more complex is often not a good solution, due to the way Havok converts them into collision shapes.

### E023
```
SEUT: Empty '{variable_1}' has incorrect rotation value: {variable_2}
```
**Cause**

The specified empty is not rotated to a valid angle.

**Solution**

Space Engineers only supports a limited amount of rotation combinations for mirroring. In some cases this means that even though the empty is rotated to the correct angle, this error still appears. Try rotating the empty to the same end position but with different rotation values on the axii. 

### E024
```
SEUT: Collection 'Mountpoints ({variable_1})' not found. Disable and then re-enable Mountpoint Mode to recreate!
```
**Cause**

The `Mountpoints`-collection of the specified scene was not found.

**Solution**

Disabling and re-enabling `Mountpoint Mode` will recreate the collection.

### E025
```
SEUT: Cannot create highlight empty for object outside of 'Main' collection.
```
**Cause**

The selected object is outside of the scene's `Main`-collection when attempting to create a `highlight empty`.

**Solution**

Move the target object of the `highlight empty` to the scene's `Main`-collection or select another object within the `Main`-collection.

### E026
```
SEUT: Filename incorrect: BLEND-filename must start with 'MatLib_' to create a valid MatLib.
```
**Cause**

The name of the MatLib's `BLEND` file must start with 'MatLib_'.

**Solution**

Rename the current `BLEND`-file so that its name starts with 'MatLib_'.

### E027
```
SEUT: 'Mountpoints {variable_1}' not found. Disable and then re-enable Mountpoint Mode to recreate!
```
**Cause**

The `Mountpoint Empty` for the specified side was not found.

**Solution**

Disabling and re-enabling `Mountpoint Mode` will recreate the empty.

### E028
```
SEUT: Object is not an Armature.
```
**Cause**

The active object is not an Armature.

**Solution**

Do not attempt to run this action on an object that is not an Armature.

### E029
```
SEUT: No Armature selected.
```
**Cause**

No Armature is currently selected.

**Solution**

Select an Armature before attempting this action.

### E030
```
SEUT: Path is directory, not EXE.
```
**Cause**

The specified path is a directory and does not point to an `EXE`-file, as required.

**Solution**

Select an `EXE`-file instead of a directory through the file-browser.

### E031
```
SEUT: Cannot export collection '{variable_1}' if it has more than one top-level (unparented) object.
```
**Cause**

The specified collection has more than one top-level object. In order for empties to work ingame, that cannot be the case and as such SEUT enforces only a single top-level object in this collision.

**Solution**

Parent all objects in the specified collection to a single object. See [this YouTube tutorial](https://www.youtube.com/watch?v=GS452KMVWKA) for a guide on object parenting in Blender 2.80+.

![](/modding-reference/assets/images/tools/seut/troubleshooting_E031.png)

### E032
```
SEUT: Object '{variable_1}' does not have valid UV-Maps. This will crash Space Engineers.
```
**Cause**

The specified object either has no UV-Maps or duplicate UV-Maps. Either will cause Space Engineers to crash, thus SEUT prevents the export.

**Solution**

Correct the specified object's UV-Maps.

### E033
```
SEUT: Invalid character(s) detected. This will prevent a MWM-file from being generated. Please ensure that no special (non ASCII) characters are used in SubtypeIds, material names and object names.
```
**Cause**

Special (non-ASCII) characters are present in `SubtypeId`s, material names or object names of scenes that were attempted to be exported. This is not allowed.

**Solution**

Go through the names specified above and ensure no special characters are present, then attempt to export once again.

### E034
```
SEUT: Collision object '{variable_1}' has unapplied modifiers. Collision model cannot be created.
```
**Cause**

The specified collision object has unapplied modifiers and cannot be exported.

**Solution**

Apply all modifiers on the specified collision object.

### E035
```
SEUT: There was an error during export caused by {variable_1}. Please refer to the logs in your export folder for details.
```
**Cause**

An unspecified error occurred during export with the specified tool.

**Solution**

Ensure that the correct tool paths are linked in the addon's preferences.