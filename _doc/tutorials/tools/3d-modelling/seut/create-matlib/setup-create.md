---
title: I. Setup & Creation
---
1. First off, the way the SEUT MatLibs are generally set up is with spheres that **display each material** contained within the MatLib. This makes it easier for users to **find and select** the material they want. But this can be any type of mesh really. Either way, create an object to assign the material to.

2. Create your material by referencing the [*&nbsp;*{: .fa .fa-map}Material Creation Tutorial](/modding-reference/tutorials/tools/3d-modelling/seut/create-material) or by using Blenders `File --> Append`-functionality to import the material into the file.

    ![](/modding-reference/assets/images/tutorials/seut/create-matlib_append.png)
<br><br/>

3. Assign your material to the mesh used to display materials in your MatLib.

4. Repeat this process for as many materials as you would like this MatLib to contain.

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Ensure that all materials in your MatLib have `Fake User` toggled and that none of them have the parameter `Override MatLib` activated. Furthermore, make sure that no other MatLib is linked into your MatLib once you save it - not even `MatLib_Presets`.
</div></div>


