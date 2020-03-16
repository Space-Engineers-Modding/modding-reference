---
title: II. Edit Existing Empties & Test Functionality
---
1. In order to edit the object an existing highlight empty targets, select the empty and access its `Object Data Properties`. There, you'll find a `Space Engineers Utilities`-panel, in which you can set the `Highlight Object` of the selected empty. 

    ![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_properties.png)
<br><br/>

    <div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
    </div><div class="content">
    {: .callout-title}
#### Note
    Objects that do not have the same parent as the highlight empty are not selectable as a target object. You must first move either the empty or the target object for both to be on the same level in the hierarchy.
    </div></div>

2. Adjust the name of the target object to fit the naming scheme. If you don't know what the scheme is, it might be easier to just recreate the highlight empty, as that will automatically rename the target object.
<br><br/>

3. Export the block and place it in your mod to load into your savegame. Then test whether everything works by placing your crosshair over the area where the empty is located and your highlight object should be highlighted.

    [![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_goal.png){:class="img-responsive-thumbnail"}](/modding-reference/assets/images/tutorials/seut/interaction-highlight_goal.png)