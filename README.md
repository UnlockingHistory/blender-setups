# blender-setups
Blender example setups for generating renderings from Virtual Unfolding

In all these test files I've set up an [orthographic camera](https://en.wikipedia.org/wiki/Orthographic_projection) with an (isometric projection](https://en.wikipedia.org/wiki/Isometric_projection).

**IMPORTANT**: The newest version of Blender (`2.91.2` at the time of writing this) does not support voxel textures in either of Eevee or Cycles rendering engines.  I rolled back to Blender `2.79` on MacOS to do these, volumetric rendering will not work on a version >`2.8`.  I have only tested the rest of these files in `2.79`.

## VolumetricRendering.blend

This is an example file that lets you create a [volumetric rendering](https://docs.blender.org/manual/de/2.79/render/blender_render/materials/special_effects/volume.html) of CT data.  First, you will need to create a .raw file to import your data into blender.  Find more info about this using the [TOMtoRAW script](https://github.com/UnlockingHistory/virtual-unfolding/tree/main/src/visualization#tom_to_raw).

A really nice tutorial about setting up these types of renders is given in [Voxel Datacubes for 3D Visualization in Blender by Matías Gárate](https://iopscience.iop.org/article/10.1088/1538-3873/129/975/058010#paspaa4f5bs4).

When you go to add your own .raw file to this blender template, you'll need to tell blender the resolution of your data under Cube>Texture>Voxel Data - mine happened to be a 58x58x58 voxel cube:

![blender voxel data resolution ui](docs/rawres.png)

Be sure to also change the dimensions of the cube to match the aspect ratio of your data.  By scaling up the size of the cube, you can increase the resolution of the resulting render.


