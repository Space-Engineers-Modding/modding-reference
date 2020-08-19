---
title: Add Dummy
---
Dummies are empties which **mark the position or presence** of a **certain functionality** within a Space Engineers model. Refer to the [*&nbsp;*{: .fa .fa-map}Dummy Tutorial]() to learn how to use dummies.

### Dummy Type
The dummy type of the empty determines what its effect will be ingame. Valid types are:

<div class="table-responsive">

{: .table .table-bordered}
| Type | Description | Note(s) | Warning(s)
|-
| **Conveyorline** | Conveyor connection point without direct access. Does not highlight anything. | Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect. | 
| **Conveyorline Small** | Small conveyor connection point without direct access. Deos not highlight anything. | Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect. | 
| **Conveyorline In** | Conveyor connection point without direct access that only lets items pass into the block. Does not highlight anything. | Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect. | 
| **Conveyorline Out** | Conveyor connection point without direct access that only lets items pass out of the block. Does not highlight anything. | Conveyor empties in a block must overlap point of origin of conveyor empty in adjacent block to connect. | 
| **Connector** | Adds connector functionality. |  | Cannot be placed too far from block origin or the connector will only spin grids instead of connecting.
| **Ejector** | Adds ejector functionality. |  | 
| **Collector** | Adds collector functionality. |  | 
| **Merge Block** | Adds merge block functionality. |  | 
| **Thruster Flame** | Determines the point where the thruster flame will appear. | Empty size defines flame width. Flame length is controlled within the SBC definition. Flare will only appear on empty with lowest index. | Thrust direction is always the Y+ axis.
| **Muzzle Missile** | The point of origin for missiles shot by the block. | Should be placed with some distance to mesh, otherwise missiles can collide with geometry of launcher. | Shoot direction is always the Y+ axis.
| **Muzzle Projectile** | The point of origin for projectiles shot by the block. |  | Shoot direction is always the Y+ axis.
| **Respawn Point** | The location in which players will respawn. Tends to place player origin (feet) to middlepoint of empty. |  | 
| **Light** | Point of origin for a light source. Does not cast shadows. |  | 
| **Camera** | Overrides default camera position at origin. |  | 
| **Upgrade Module** | Marks slots where upgrade modules can be placed. |  | 
| **Air Vent** | Adds air vent functionality. |  | 
| **Landing Gear** | Adds landing gear functionality. Any geometry within the empty will be a valid lock target - not only near the point of origin. |  | 
| **Ship Tool** | The point of origin for ship tool effects (not visual). |  | 
| **Electric Motor** | The location onto which a rotor head or wheel will be placed. |  | 
| **Character** | The location in which the character model will be placed. Point of origin is generally aligned with the butt of the character but this can depend on the pose. |  | 
| **Particles 1** | Point of origin for particles (used in grinder and welder). |  | 
| **Particles 2** | Point of origin for particles (used in grinder). |  | 
| **Piston Top** | The top part of a piston. |  | 
| **Wheel** | The position at which a wheel is connected to a suspension. |  | 
| **Center** | Defines the center of a block. |  | 

</div>

### Index
Index defines the numeric index of a dummy and its object counterpart. Not supported by all dummies.

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Ensure that there are no two empties of the same type with the same index. This will cause issues.
</div></div>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>
