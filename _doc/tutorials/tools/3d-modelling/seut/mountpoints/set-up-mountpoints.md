---
title: I. Set up Mountpoints
---
1. Update the `Bounding Box` of your scene to completely encompass your model.

    ![](/modding-reference/assets/images/tutorials/seut/mountpoints_bbox.png)
<br><br/>

2. Activate `Mountpoint Mode` through the SEUT [*&nbsp;*{: .fa .fa-database}Main Panel](/modding-reference/reference/tools/3d-modelling/seut/main-panel#mountpoint-mode).

    ![](/modding-reference/assets/images/tutorials/seut/mountpoints_activate.png)
<br><br/>

3. Select and modify the **turquoise planes** that are placed around your model **in Blender's** `Object Mode`. These are the `Mountpoint Areas`, of which there can be multiple per `Mountpoint Side`. **Sides are represented by the empties** spawned around your model - Areas are parented to them. You can **move, scale and delete** `Mountpoint Areas` but if they reach over the sides of the bounding box, the excess is trimmed on save.

    ![](/modding-reference/assets/images/tutorials/seut/mountpoints_edit-areas.png)
<br><br/>

    <div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
    </div><div class="content">
    {: .callout-title}
#### Warning
    Rotation of `Mountpoint Areas` is not saved as SEUT uses the bounding box of the area to save its size. There is **no real way to properly define diagonal mountpoint areas** of any kind for Space Engineers, as such SEUT does not support it either.
    </div></div>

4. You can also add more `Mountpoint Areas` to a `Mountpoint Side` by using the `Add Area`-button in the `Main Panel` with the respective side's empty selected. There is no hard limit on the amount of Areas you can add per Side, but **too many will have a negative effect on performance**.

    ![](/modding-reference/assets/images/tutorials/seut/mountpoints_add-areas.png)
<br><br/>

5. Deactivate `Mountpoint Mode` to save the values. On export, the results will be written into the generated `SBC`-file. 
<br><br/>