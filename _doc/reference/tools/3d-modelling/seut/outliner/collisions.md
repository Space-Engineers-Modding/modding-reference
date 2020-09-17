---
title: Collisions
---

This collection will allow you to specify collison meshes for your object.

### Convex Hulls

The most flexible and basic collsion type available to your collision meshes is the Convex Hull. As stated in the name, this mesh is convex, and cannot be concave in any way. 
<br><br/>
This image should shed some light on what is valid:

![](/modding-reference/assets/images/reference/seut/collisionmesh1.png)

Creating a valid convex collison mesh requires basically no setup from you, the Rigidbody Physics Property is applied for you on export, if none is present. For creating more specialized types of collisions, see the next section.
<br><br/>

### Other Types

The physics compiler can accept a few other collision methods along with convex, here are a few that we know:
<br><br/>

* **Cylinder** - Has its uses, kind of like convex hull but purpose made for cylinders, the hinges are a good example of their use.
* **Sphere** - Spherical collision, good for wheels and whatever else you need it for.
* **Box** - Very simple, basic box collision.

<br><br/>

Changing your collision mesh to one of these types is very easy:

![](/modding-reference/assets/images/reference/seut/collisionmesh2.png)

<br><br/>

<div class="callout-block callout-warning"><div class="icon-holder">*&nbsp;*{: .fa .fa-bug}
</div><div class="content">
{: .callout-title}
#### Warning
Your collision meshes **MUST have their transformations applied!** Otherwise you will get undesired behavior ingame, due to the origin point of your collision mesh being offset from the center of the scene. You can apply your object's transforms by doing the following in Object Mode: `Ctrl-A --> All Transforms`
</div></div>

<br><br/>
<p style="text-align:right">[*&nbsp;*{: .fa .fa-database} Back to SEUT Reference](../seut.html){: .btn .btn-blue}</p>