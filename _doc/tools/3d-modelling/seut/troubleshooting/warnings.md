---
title: SEUT Warnings
---

### W001
```
SEUT: Collection not found. Action not possible.
```
**Cause**

A collection could not be found to perform a specified action.

**Solution**

This can generally be ignored. To resolve this warning, press the `Recreate Collections`-button in the [*&nbsp;*{: .fa .fa-database}SEUT Main Panel](/modding-reference/reference/tools/3d-modelling/seut/main-panel#recreate-collections).

### W002
```
SEUT: Collection '{variable_1}' excluded from view layer or empty. Action not possible.
```
**Cause**

The specified collection is excluded from the view layer.

**Solution**

This can generally be ignored. To resolve this warning, if the collection is excluded, tick the collection's checkbox in the outliner:
  
![](/modding-reference/assets/images/tools/seut/troubleshooting_E002.png)

If the specified collection is empty, place at least one object into the collection.

### W003
```
SEUT: Could not remove unused material slots for object '{variable_1}'.
```
**Cause**

There was an unspecified issue when attempting to remove unused materials from the listed object.

**Solution**

This can generally be ignored. To resolve, attempt to manually remove the unused materials from the specified object.

### W004
```
SEUT: '{variable_1}' texture of local material '{variable_2}' is not of a valid resolution ({variable_3}). May not display correctly ingame.
```
**Cause**

The texture resolution of the specified texture has an invalid resolution. Space Engineers only supports resolutions that are to the power of 2: 128x128, 256x256, 512x512, 1024x1024 etc.

**Solution**

Edit your texture to have a valid resolution.

### W005
```
SEUT: Empty '{variable_1}' (numbering might differ) in collection '{variable_2}' has no parent object. This may prevent it from working properly ingame.
```
**Cause**

The specified empty (though the '.001' number at the end of its name might differ) has no parent object. This will generally prevent it from working within Space Engineers.

**Solution**

Ensure the specified empty is parented to the top-level object of the listed collection.

### W006
```
SEUT: Parent of empty '{variable_1}' (numbering might differ), '{variable_2}', in collection '{variable_3}' has a parent object. This may prevent the empty from working properly ingame.
```
**Cause**

The listed parent of the specified empty (though the '.001' number at the end of its name might differ) has its own parent object. This means that the empty is not parented to the listed collection's top-level object.

**Solution**

Ensure that the specified empty is parented to the listed collection's top-level object.

![](/modding-reference/assets/images/tools/seut/troubleshooting_W006.png)

### W007
```
SEUT: Highlight empty '{variable_1}' (numbering might differ) and its linked object '{variable_2}' have different parent objects. This may prevent the empty from working properly ingame.
```
**Cause**

The specified empty (though the '.001' number at the end of its name might differ) has a different parent object from its target object. This will generally prevent it from working within Space Engineers.

**Solution**

Ensure the specified empty is parented to the same parent object as its target object.

### W008
```
SEUT: Scene '{variable_1}' is of type '{variable_2}' but does not contain any armatures.
```
**Cause**

The specified scene is of a type that supports armatures but does not contain any.

**Solution**

Either switch the specified scene to a different type or add armatures to the scene.

### W009
```
SEUT: Scene '{variable_1}'  is of type '{variable_2}' but contains armatures.
```
**Cause**

The specified scene is of a type that doesn't support armatures but contains them.

**Solution**

Either switch the specified scene to a different type or remove the armatures from the scene.

### W010
```
SEUT: Library '{variable_1}' could not be relocated in '{variable_2}'.
```
**Cause**

The specified previously linked MatLib could not be found anymore in the specified folder.

**Solution**

Unless the MatLib was removed intentionally, in which case this can be ignored, check the specified folder and replace the MatLib `BLEND`-file.