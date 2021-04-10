---
title: Overview
---
![](/modding-reference/assets/images/reference/seut/collections.png)

### Collection Breakdown
Here's a quick reference of all the collections that SEUT creates, and how they are used!

* **Main** - This collection contains the main mesh of your model.
* **Collision** - These collections contains the collision mesh (or meshes) of your model.
* **BS1-X** - These collections contains your block's build stages, these are referenced in the SBC file of your block.
* **LOD1-X** - These collections contains the various "Levels of Detail" of your model.
* **BS_LOD** - This collection contains one LOD that will show when your block is in a construction state.

<br><br/>

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
All objects in every collection (except for the **Collision** collection) **must be parented to one top-level object**. Measures have been implemented to ensure that you are made aware of this on export, but still be aware.
</div></div>

