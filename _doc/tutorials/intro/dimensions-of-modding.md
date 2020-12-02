---
title: I. Dimensions of Modding
sections:
  - SBC modding
  - Scripting
  - Modding assets
---
As newcomers to modding a specific game, oftentimes people will not be aware of what can and cannot be modded in the first place. And what use are the greatest plans for a mod if the game developer has disallowed access to the key files needed to make those plans reality? This chapter will expand on the "three dimensions" of modding, which each require their own expertise and tools. Knowing about these different dimensions will allow you to better understand which are relevant for your plans, and which you'd be interested in learning.

# SBC modding
SBC is a filetype that Space Engineers uses to save moddable data in. It contains a XML data structure. Editing these files and the information contained within is the easiest form of modding for SE. SBC modding allows the addition of more content to the existing "framework" available in the vanilla game, but it does not allow for changing said framework. For example, while you can add more blocks using SBC modding, you would not be able to give these blocks a functionality that does not already exist for another block currently in the game.

### Example
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
Scripting is what is used to change and extend the "framework" mentioned in the last section. It is done in C# (CSharp), a programming language that is very common and is widely used outside of Space Engineers. If you have prior knowledge of programming, this is a pretty good place to start. If you do not, you may want to reconsider starting with this dimension of modding. Learning a programming language and the algorithms and logic to successfully create a script for SE is not something that can be learned in just a month or two. The good news is, however, that there are a lot of C# tutorials available for free online.

### Example
```cs
public class Container : MyGameLogicComponent
    {
        IMyThrust m_block;

        private string EMISSIVE_MATERIAL_NAME = "Emissive";
        private Color GREEN = new Color(0, 255, 0);
        private Color RED = new Color(255, 0, 0);
        private Color lastColor;


        bool IsWorking
        {
            get
            {
                return m_block.IsWorking;
            }
        }

        public override void Init(MyObjectBuilder_EntityBase objectBuilder)
        {
            NeedsUpdate |= MyEntityUpdateEnum.EACH_10TH_FRAME;

            m_block = Entity as IMyThrust;
        }
```
**Source:** A section of a script used to change the color of the glowing parts of a thruster in a mod.

## Programmable Block
Scripts can also be written for the Programmable Block inside of Space Engineers. It's largely identical to general scripting for the game, albiet more restrictive to prevent players from exploiting the game using those scripts.

### Example


## Visual Scripting
Visual Scripting is a form of scripting that does not require the user to write actual code. The code is instead represented in the form of a network of nodes that are connected to each other. As a result, it's much more approachable for newbies, but the tool used to create these visual scripts - Visual Scripting Tool (VST) - is unfortunately still somewhat buggy. Furthermore, while it does not require the user to write actual code, knowledge of algorithms and the logic under which programs operate is still absolutely essential.

### Example
![](/modding-reference/assets/images/tutorials/intro/vst.png)

# Modding assets
Modding assets refers to creating or editing anything that is not pure data or code in Space Engineers. While it doesn't require as much prior knowledge to produce usable results with, modding assets does instead oftentimes require a lot of different applications to produce content with. While the industry standard applications are generally very expensive, there are usually alternatives available that can produce similar results for free - albiet they may require you to clear a couple additional hurdles in the process.

## 3D modelling
3D modelling is not an easy skill to learn but there are many applications and much more tutorials available on the internet. 3D modelling is creating objects in SE. Be it blocks, tools, components or even player characters - they were all created in a 3D modelling application.

### Example
![](/modding-reference/assets/images/tutorials/intro/3d-modelling.png)

## Texture modding
Textures are what determine the colors of 3D models in games. They can be edited separately from 3D models and require a separate set of applications to mod. This is one of the easier disciplines and a pretty good point to start with should you want to look into modding the game's visuals.

### Example
