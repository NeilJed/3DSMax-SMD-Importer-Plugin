
# 3D Studio Max SMD import plug-in
A plug-in for Autodesk 3D Studio Max for importing SMD format files, popular with Half-Life and Source based games.

## Overview
This plug-in allows 3D Studio Max to import SMD format files used primarily in Half-Life and Source engine based games. However the format has been adopted as an intermediate format by various other 3D games and tools. It can import reference and sequence SMD files for use when compiling models along with extra features to ease workflow.

## Features
* SMD triangles are rebuilt as a solid, continuous mesh removing the need for vertex welding.
* Recreates smoothing using vertex normal data.
* Creates a multi/sub-object material and assigns material IDs to faces.
* Creates bone "nodes" and re-builds the skeleton hierarchy.
* Supports import of animation including reference frame only and reversal.
* Option to represent certain bones as dummy objects.
* Skinning of the mesh and skeleton with imported SMD vertex weights.
* Coordinate space mapping to "stand up" models made with Maya.

## Supported versions
3DS Max 2017 - 64bit
3DS Max 2018 - 64bit
3DS Max 2019 - 64bit
3DS Max 2020 - 64bit

## Installation
Copy the `SMDImporter.dle`file for the correct version for your edition of 3D Studio Max into your 3DS Max plug-ins folder (i.e. `C:\Program Files\Autodesk\3ds Max 2020\Plugins`) and re-start. You can check it's loaded via the Plug-ins Manager.

## Basic usage
Once installed, using the *Import* option of the File menu you should find *Valve SMD* as an option.

The first dialog gives you the option to skip the Mesh or Animation sections of the SMD. This is useful if you have a very large SMD file or an exceptionally slow computer. The main options dialog has various options on how to recreate the model on import. Each option has a tool-tip that explains it's purpose.

## Tips & tricks

**When I import my model, it’s all grey with no texture.**

While the importer creates multi/sub-object material for the model it can only set the filename for the texture from the SMD. Because of this Max doesn’t know where to find the texture file and can’t display it.

To correct the problem, open the materials browser and use the picker to get the models material. For each sub material select the diffuse texture and browse to where the actual texture file is. Once done the texture should appear.

**My model is smooth but has no smoothing groups?**

The importer uses explicit vertex normals to recreate the smoothing exactly as defined in the SMD. The removes the need for smoothing groups and gives much more control. If you want to edit them add a Edit Normals modifier to your stack.

**I don’t want to use vertex normals, how do I add/use smoothing groups?**

First you’ll have to clear the vertex normals. You can either do this by re-importing the SMD with the smoothing normals option turned off or place an Editable Poly modifier on top of the stack. Once this is done you can then set the smoothing groups manually.

**I’m using vertex normals for smoothing but when I export my model comes out flat shaded.**

Make sure you have the latest version of the SMD exporter plug-in. Version 1.4 onwards supports explicit vertex normals.

**My model is lying on it’s back when I import it.**

This usually happens when original SMD was exported from Maya. Use the “Convert from Left-Handed” import option.

## Legal

### Author
This software was created by and is &copy; 2011 Neil "Jed" Jedrzejewski

### License & Warranty
The content owner grants a non-exclusive, perpetual, personal use license to view, download, display, and copy the content, subject to the following restrictions:

1. The content is licensed for personal and non-profit use only, not commercial use. The content may not be used in any way whatsoever in which you charge money, collect fees, or receive any form of remuneration for commercial gain. The content may not be resold, relicensed, sub-licensed, rented, leased, or used in advertising.

2. Title and ownership, and all rights now and in the future, of and for the content remain exclusively with the content owner.

3. This software is provided 'as-is', without any express or implied warranty.

4. The content owner will not be liable for any third party claims or incidental, consequential, or other damages arising out of this license or the use of the content.

5. This notice must NOT be removed or altered from any distribution of this software.
