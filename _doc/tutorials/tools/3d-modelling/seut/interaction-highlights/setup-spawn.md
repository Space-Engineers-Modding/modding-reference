---
title: I. Setup Model & Spawn Empty
---
1. First of all, your blend file must of course contain the SEUT standard collections, specifically the `Main`-collection, and your model must be placed within it.
<br><br/>

2. Next, you will have to ensure that all separate parts of your model are parented to a single object or empty. As you can see in the following picture, all individual parts of my example model are parented to the empty named "Model".

    ![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_structure.png)
<br><br/>

3. In order to highlight an area of your block when the player interacts with it, you first need to define an interactable area. This is done by placing a specific empty though the [*&nbsp;*{: .fa .fa-database}Add / Context Menu](/modding-reference/reference/tools/3d-modelling/seut/add-context-menu) by first selecting the object you wish to be highlighted and then going to `Add --> Create Empty --> Add Highlight Empty`.
<br><br/>

4. A menu will appear in the bottom left of your `3D Viewport`. Select the type of interaction you would like to be accessible through this surface. In my case, I want to add a highlight for the conveyor port so I choose `Conveyor`. The index is needed to differentiate multiple empties of the same type and you'll need to ensure that you **don't have two empties of the same type with the same index number**. Note that the object you selected initially will also get renamed in order to facilitate the connection between the empty and the object it highlights.

    ![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_popup.png)
<br><br/>

    <div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
    </div><div class="content">
    {: .callout-title}
#### Note
    All listed highlight empties have hover-texts assigned to them containing more information. Simply move your cursor over the item in the list.
    </div></div>

5. Resize your empty to comfortably encompass the surface you would like to be highlighted. The empty defines the area where the crosshairs must be placed in order for the outline to appear. Dont' forget to apply transformations after you've resized and moved the empty.

    ![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_setup.png)