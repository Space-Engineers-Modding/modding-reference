---
title: II. Troubleshooting
sections:
  - Testing Mountpoints Ingame
  - Mountpoints are Completely Misaligned in Blender
---
### Testing Mountpoints Ingame
It is possible to view the mountpoints ingame by accessing the Debug menu using Alt + F11. However, that is not always available in a savegame and the mountpoints are somewhat hard to see. Instead, it is recommended to make use of [Digi's BuildInfo](https://steamcommunity.com/sharedfiles/filedetails/?id=514062285) mod. 

Toggle its overlays with the corresponding keybinding while holding the block for placement to show both the block's directions as well as the mountpoints (in yellow):

![](/modding-reference/assets/images/tutorials/seut/mountpoints_test.png)

### Mountpoints are Completely Misaligned in Blender
You can test how mountpoints have been saved by toggling `Mountpoint Mode` off and back on again. If your mountpoint areas are completely misaligned when you do that, the reason is often that you have edited them in `EDIT`-mode but not applied transformations afterwards. It is recommended to make adjustments to mountpoint areas in `OBJECT`-mode, as that does not require applying transformations afterwards.

Note that mountpoint areas cannot be rotated, as they are saved as X and Y coordinates.

<br><br/>

<p style="text-align:right">[*&nbsp;*{: .fa .fa-map} Back to SEUT Tutorials](../seut.html){: .btn .btn-green}</p>