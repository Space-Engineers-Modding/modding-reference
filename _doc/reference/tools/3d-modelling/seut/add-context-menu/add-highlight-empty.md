---
title: Add Highlight Empty
---
Highlight empties define which part of a model is **highlighted** when the player points the crosshairs at the area the highlight empty encompasses. Refer to the [*&nbsp;*{: .fa .fa-map}Highlight Empty Tutorial](/modding-reference/tutorials/tools/3d-modelling/seut/interaction-highlights) to learn how to use these empties.

<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
In order to add a highlight empty, you must have the object it should highlight selected. If you have no object selected, the `Add Highlight Empty`-option will be **greyed out**.
</div></div>

### Highlight Type
The highlight type of the empty decides its functionality ingame. Valid types are:

<div class="table-responsive">

{: .table .table-bordered}
| Type | Description | Note(s)
|-
| **Conveyor** | Defines large conveyor access point. | Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect.
| **Small Conveyor** | Small Conveyor, Defines small conveyor access point. | Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect.
| **Terminal** | Defines terminal access point. | 
| **Text Panel** | Defines access points for LCD Text Panels. | 
| **Button** | Defines access points for single buttons. | 
| **Cockpit** | Defines access point to block that can be entered. | 
| **Door** | Defines door access point. | 
| **Advanced Door** | Defines advanced door access point. | 
| **Medical Station** | Defines access point to part of medical station that allows for health / o2 / h2 / energy regeneration. | 
| **Wardrobe** | Defines access point to part of medical station that allows the switching of skins. | Moves player to within the empty and disables jetpack. May require geometry above and below so player does not fall due to gravity.
| **Cryopod** | Defines cryopod access point. | 
| **Inventory** | Defines inventory access point (without conveyor functionality). | 

</div>

### Index
Index defines the numeric index of a highlight empty and its object counterpart.

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Ensure that there are no two empties of the same type with the same index. This will cause issues.
</div></div>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>
