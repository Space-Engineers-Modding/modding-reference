---
title: I. Setup Model & Spawn Empty
---
1. First of all, your blend file must of course contain the SEUT standard collections, specifically the `Main`-collection, and your model must be placed within it.
<br><br/>

2. Next, you will have to ensure that all separate parts of your model are parented to a single object or empty. As you can see in the following picture, all individual parts of my example model are parented to the empty named "Model".

    ![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_structure.png)

3. In order to highlight an area of your block when the player interacts with it, you first need to define an interactable area. This is done by placing a specific empty though the [*&nbsp;*{: .fa .fa-database}Add / Context Menu](/modding-reference/reference/tools/3d-modelling/seut/add-context-menu) by first selecting the object you wish to be highlighted and then going to `Add --> Create Empty --> Add Highlight Empty`.
<br><br/>