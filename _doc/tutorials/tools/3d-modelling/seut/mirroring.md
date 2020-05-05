---
title: Mirroring Tutorial
excerpt: Tutorial about the SEUT functionality for setting up mirroring for blocks.
date: 2020-03-10
icon:
  type: fa
  name: fa-cube
color: green
sections:
  - /tutorials/tools/3d-modelling/seut/mirroring/set-up-mirroring
  - /tutorials/tools/3d-modelling/seut/mirroring/troubleshooting
---

<div class="table-responsive">

{: .table .table-bordered}
| This tutorial teaches you how to set up the correct **mirroring behaviour** for a block. This has the effect of the block being placed with the **correct rotation when using mirroring mode** for building within Space Engineers.

</div>

### Goal
To get a block to correctly mirror its rotation when using mirroring mode in Space Engineers creative building.

[![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_goal.png){:class="img-responsive-thumbnail"}](/modding-reference/assets/images/tutorials/seut/mirroring_goal.png)

### Prerequisites
* A suitable block to set up mirroring with.

<br><br/>

<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
There is **no real mirroring** in Space Engineers. Mirroring is achieved by defining which ways a block should be rotated to achieve something that looks like a mirrored block on the other side of the mirror axis. But this only works for blocks that are symmetrical on at least one axis. Should that not be a case, it is necessary to define a `Mirror Model`.
</div></div>

<br><br/>