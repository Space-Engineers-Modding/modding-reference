---
title: II. Troubleshooting
sections:
  - Empty has incorrect rotation values
  - Huge geometry appears when Mirroring Mode is enabled
  - Rotating the empty to correctly mirror the block on all axi is impossible
  - Mirroring ingame is wrong
---
### Empty has incorrect rotation values.
You might get an error message informing you that one of your empties have an incorrect rotation value. This is because the possible rotations (combination of rotations for each of the three axi on an empty) are *predetermined*. 

For the `SBC` output, they are converted into text to tell the game how to interpret them. But this also means that **there is a list of text associated with rotation values**. If the rotation you've ended up with is **not "available"** in this list, it **cannot be read by the game**.

To avoid this, make sure you always rotate in 90° increments. Your axi rotation values will generally be -/+ 90° or -/+ 180°. Note that 270° is the same as -90°.


<div class="callout-block callout-info"><div class="icon-holder">*&nbsp;*{: .fa .fa-info-circle}
</div><div class="content">
{: .callout-title}
#### Note
Sometimes this error appears **even if you have entered the seemingly correct values**, with the instances looking to be rotated correctly. This can be a limitation of the system: That particular combination might just **not be defined** in Keen's rotation value set. To get around this, simply **try different axi rotations** that end up with the instance **facing the same way**.
</div></div>


### Huge geometry appears when Mirroring Mode is enabled.
This commonly happens if you work with vanilla Space Engineers models from the Mod SDK. 

![](/modding-reference/assets/images/tutorials/seut/mirroring_huge-objects.png)

The reason for this is that Keen tends to model in 10x size and then scale the top object (that all other objects are parented to) down to 0.1 . This then also scales down all child objects. Because of the method SEUT uses to create an instance, **this parenting is not applied to the instances** and so the child objects are displayed in their original size.

This is a **purely visual issue** for the duration that `Mirroring Mode` is activated. After the mode is deactivated, the instances are cleared up and the problem disappears - **there is no lasting damage to your model**.

In order to fix this issue, do the following:

1. Turn off `Mirroring Mode`.

2. `Apply Transformations... Scale` (Select object, `Ctrl + A`) on the object that is scaled down (which the other objects are parented to).

3. Turn `Mirroring Mode` back on. The huge objects should be gone.
<br><br/>

### Rotating the empty to correctly mirror the block on all axi is impossible.
In some cases it is straight-up impossible to rotate the model in a manner that successfully creates a mirror. This is generally the case when the model is not symmetrical on any axis. If this is the case for your model, you will need to define a `Mirror Model`. 

A `Mirror Model` is set up by creating another scene in the same `BLEND`-file, which is then set to the Scene Type `Mirroring`: 

![](/modding-reference/assets/images/tutorials/seut/mirroring_scene-type.png)

In this scene, set up a copy of your main scene but **use the Blender tools to mirror the model** on an axis. You will have to add this mirror model as a separate block to the game. Next, set this new (mirror) scene as the `Mirror Model` in your main scene:

![](/modding-reference/assets/images/tutorials/seut/mirroring_mirror-model.png)

This will then update the displayed instances below the rotation empties to the newly linked scene's main collection. On export, this will be written to the `SBC`file and ingame it will automatically display your mirror model - provided it has also been correctly added to the mod.

<br><br/>

### Mirroring ingame is wrong.
This is fairly unlikely to happen if none of the other problems here have appeared beforehand. Know that mirroring values are saved when you either exit `Mirroring Mode` or export your scene. As a result, if you want to verify that your rotation values are correct, first exit `Mirroring Mode` and then enable it once again. If the rotation empties and instanced models are still facing the same / the correct directions, it should work perfectly ingame.


<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Make sure you don't forget to update the `SBC` in your mod folder with the new rotation values!
</div></div>

<br><br/>

<p style="text-align:right">[*&nbsp;*{: .fa .fa-map} Back to SEUT Tutorials](../seut.html){: .btn .btn-green}</p>