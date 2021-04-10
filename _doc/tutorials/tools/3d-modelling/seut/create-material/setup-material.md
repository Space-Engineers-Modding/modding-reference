---
title: II. Setup Material
---
1. Use the `Create SEUT Material`-button to create the node tree for your material.

    ![](/modding-reference/assets/images/tutorials/seut/create-material_button.png)
<br><br/>

2. In the `Shader Editor`, link the individual texture files (in any format that Blender can read) to their respective image nodes in the material. Also don't forget to name your new material.

    ![](/modding-reference/assets/images/tutorials/seut/create-material_nodes.png)
<br><br/>

3. In the SEUT `Shader Editor Panel`, define **additional parameters** for your material. You can find the explanation for what each one does in the [*&nbsp;*{: .fa .fa-database}Shader Editor Panel Reference](/modding-reference/reference/tools/3d-modelling/seut/shader-editor-panel#preset). 

    ![](/modding-reference/assets/images/tutorials/seut/create-material_params.png)
<br><br/>

    <div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
    </div><div class="content">
    {: .callout-title}
#### Note
    Materials with the technique `GLASS` can have more parameters defined in the `TransparentMaterials.sbc`. SEUT does currently not support output for it though.
    </div></div>

4. Be sure to toggle the setting for `Fake User` for the material. This will ensure that the material **does not get deleted** if it isn't assigned to any part of your model and you load a `BLEND`-file into Blender.

    ![](/modding-reference/assets/images/tutorials/seut/create-material_fakeuser.png)
<br><br/>

5. Lastly, if your material uses a `NG` texture, be sure to set the `Color Space` of the image node to `Non-Color`.

    ![](/modding-reference/assets/images/tutorials/seut/create-material_colorspace.png)
<br><br/>

    <div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
    </div><div class="content">
    {: .callout-title}
#### Note
    If you have created a material (or several materials) you wish to **use across multiple** `BLEND`-files, consider setting up a `MatLib` for it. Doing so will make handling the material **a lot easier**. Find out how to do that in the [*&nbsp;*{: .fa .fa-map}Create MatLib Tutorial](/modding-reference/tutorials/tools/3d-modelling/seut/create-matlib).
    </div></div>

