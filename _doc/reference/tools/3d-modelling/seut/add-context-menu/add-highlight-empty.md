---
title: Add Highlight Empty
---
Highlight empties define which part of a model is **highlighted** when the player points the crosshairs at the area the highlight empty encompasses.

<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
In order to add a highlight empty, you must have the object it should highlight selected. If you have no object selected, the `Add Highlight Empty`-option will be **greyed out**.
</div></div>

### Highlight Type
The highlight type of the empty decides its functionality ingame. Valid types are:

* **Conveyor** - Defines large conveyor access point. **Note**: Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect.
* **Small Conveyor** - Small Conveyor, Defines small conveyor access point. **Note**: Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect.
* **Terminal** - Defines terminal access point.
* **Button** - Defines access points for single buttons.
* **Cockpit** - Defines access point to block that can be entered.
* **Door** - Defines door access point.
* **Advanced Door** - Defines advanced door access point.
* **Medical Station** - Defines access point to part of medical station that allows for health / o2 / h2 / energy regeneration.
* **Wardrobe** - Defines access point to part of medical station that allows the switching of skins. **Note**: Moves player to within the empty and disables jetpack. May require geometry above and below so player does not fall due to gravity.
* **Cryopod** - Defines cryopod access point.

### Index
Index defines the numeric index of a highlight empty and its object counterpart. 
<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>
