---
title: II. Troubleshooting
---
### Huge geometry appears when Mirroring Mode is enabled.
This commonly happens if you work with vanilla Space Engineers models from the Mod SDK. 

![](/modding-reference/assets/images/tutorials/seut/mirroring_huge-objects.png)

The reason is that Keen tends to model in 10x size and then scale the top object (that all other objects are parented to) down to 0.1 . This then also scales down all child objects. Because of the method SEUT uses to create an instance, this parenting is not applied to the instances and so the child objects are displayed in their original size.

This is a purely visual issue for the duration that `Mirroring Mode` is activated. After the mode is deactivated, the instances are cleared up and the problem disappears - there is no lasting damage to your model.

In order to fix this issue, do the following:

1. Turn off `Mirroring Mode`.

2. `Apply Transformations... Scale` (Select object, `Ctrl + A`) on the object that is scaled down (which the other objects are parented to).

3. Turn `Mirroring Mode` back on. The huge objects should be gone.
<br><br/>

### Rotation values could not be saved.
--> try achieving the same overall rotation using different steps

![](/modding-reference/assets/images/tutorials/seut/interaction-highlight_old.png)

<br><br/>

### Mirroring ingame is wrong.
--> check saved rotations

<br><br/>

### Rotating the empty to correctly mirror the block on all axi is impossible.
--> Mirror Model

<br><br/>

<p style="text-align:right">[*&nbsp;*{: .fa .fa-map} Back to SEUT Tutorials](../seut.html){: .btn .btn-green}</p>