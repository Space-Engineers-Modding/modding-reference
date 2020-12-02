---
title: I. Dimensions of Modding
---
As newcomers to modding a specific game, oftentimes people will not be aware of what can and cannot be modded in the first place. And what use are the greatest plans for a mod if the game developer has disallowed access to the key files needed to make those plans reality? This chapter will expand on the different "dimensions" of modding, which each require their own expertise and tools. Knowing about these different dimensions will allow you to better understand which are relevant for your plans, and which you'd be interested in learning.

# SBC modding
SBC is a filetype that Space Engineers uses to save moddable data in. It contains a XML data structure. Editing these files and the information contained within is the easiest form of modding for SE.

## Example
```xml
    <Component>
      <Id>
        <TypeId>Component</TypeId>
        <SubtypeId>SteelPlate</SubtypeId>
      </Id>
      <DisplayName>DisplayName_Item_SteelPlate</DisplayName>
      <Icon>Textures\GUI\Icons\component\steel_plate_component.dds</Icon>
      <Size>
        <X>0.5</X>
        <Y>0.5</Y>
        <Z>0.01</Z>
      </Size>
      <Mass>20</Mass>
      <Volume>3</Volume>
      <Model>Models\Components\steel_plate_component.mwm</Model>
      <PhysicalMaterial>Metal</PhysicalMaterial>
      <MaxIntegrity>100</MaxIntegrity>
      <DropProbability>0.9</DropProbability>
      <Health>53</Health>
    </Component>
```
**Source:** `Components.sbc` - This defines the "Steel Plate" component.

# Scripting