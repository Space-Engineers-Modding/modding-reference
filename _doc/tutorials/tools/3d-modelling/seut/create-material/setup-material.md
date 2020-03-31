---
title: II. Setup Material
---
1. The first step is to ensure that you have linked the `MatLib_Presets` in the [*&nbsp;*{: .fa .fa-database}Shader Editor Panel](/modding-reference/reference/tools/3d-modelling/seut/shader-editor-panel) and to then create a new Material using the SEUT button for it.

    ![](/modding-reference/assets/images/tutorials/seut/create-material_button.png)
<br><br/>

    <div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
    </div><div class="content">
    {: .callout-title}
#### Note
    Choose the material creation preset based on what kind of material you would like to create. The main difference is what kind of texture maps are supported by the material. Find an overview over the different SEUT material types in the [*&nbsp;*{: .fa .fa-database}Shader Editor Panel Reference](/modding-reference/reference/tools/3d-modelling/seut/shader-editor-panel#preset).
    </div></div>

2. In the `Shader Editor`, link the individual textures to their respective image nodes in the material.

    ![](/modding-reference/assets/images/tutorials/seut/create-material_nodes.png)

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

5. If you have created a material (or several materials) you wish to **use across multiple** `BLEND`-files, consider setting up a `MatLib` for it. Doing so will make handling the material **a lot easier**. Find out how to do that in the [*&nbsp;*{: .fa .fa-map}Create MatLib Tutorial](/modding-reference/tutorials/tools/3d-modelling/seut/create-matlib).
<br><br/>