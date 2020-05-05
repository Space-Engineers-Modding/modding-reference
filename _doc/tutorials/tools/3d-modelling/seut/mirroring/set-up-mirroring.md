---
title: I. Set up Mirroring
---
1. Activate `Mirroring Mode` through the SEUT [*&nbsp;*{: .fa .fa-database}Main Panel](/modding-reference/reference/tools/3d-modelling/seut/main-panel#mirroring-mode).

    ![](/modding-reference/assets/images/tutorials/seut/mirroring_setup.png)
<br><br/>

2. Select the `Mirror FrontBack`, `Mirror LeftRight` and `Mirror TopBottom` empties in turn and rotate them to their correct mirrored positions. As an instance of the model contained in the `Main`-collection is placed below all three empties, it will rotate together with the empty it is parented to and as such you will be able to see what the current state of the rotation is easily.

    ![](/modding-reference/assets/images/tutorials/seut/mirroring_rotate.png)

    <div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
    </div><div class="content">
    {: .callout-title}
#### Note
    The key to understanding how `Mirroring Mode` works is to look at the spawned instances of the main model as *mirror images* of the main model, as seen through the `Mirror Planes`. This means that when looking through one of the half-transparent planes from the side of the main model, the instance you see through it should be rotated in a manner to look like the main model is reflected on the surface of the `Mirror Plane`.
    </div></div>

3. Deactivate `Mirroring Mode` to save the values. On export, the results will be written into the generated `SBC`-file.
    
<br><br/>