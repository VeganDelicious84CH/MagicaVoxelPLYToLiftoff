# MagicaVoxelPLYToLiftoff
converter to get (smaller) Magica Voxel Objects into the Liftoff Editor (the FPV Sim by LuGus Studios).
Please use Magicavoxel 0.98 if you get a strange error. Newer versions like 0.99.6 or 0.99.7 sadly don't work. Thanks for youtube user KeaiduoUsually for finding that out.

howto
1. In MagicaVoxel: under "export > point" export your model as a .PLY
2. In your File Explorer: put the PLY into the "INPUT"-folder of this converter
3. Run the PlyToLiftoff.exe or the PlyToLiftoff.py via Python
4. Output file is inside a folder (with a random name) and should go into:
   Liftioff's "tracks" folder (programs(86)>steam>>steamapps>common>liftoff>tracks)
   
In case you want to draw a MagicaVoxel object from ground up I added Liftoffs 5-colour-palette. However due to my problem with recognizing colours they might be a bit off.

what it does
- 1 block of 1x1x1 size in Liftoff is represented by 1 block in MagicaVoxel. 
- the huge colour palette of Magica is tried to be translated into Liftoffs' 5 colours.
- the script was used for something else before (Minecraft) and has a section that recalculates coords from absolute to relative (so the objects were always spawned at my feet in Minecraft) but here in Liftoff it is useless. I left that code section for now. Maybe I could instead add ad some variables to raise all blocks if they have to fit onto something else. 

issues / limitations:
- Your spawn point may be in the middle of a block. Then you can change the spawn position using Lifotff's editor
- Bigger Magica-VOX objects like "monum_2" did not work. I do not know if it is because of the filesize or maybe because of a height limitation or both.
- Other objects than the 1x1 blocks are not possible
- I have to clean up the source code a bit for better readability if you want to improve or adapt it.
- This project was originally done for converting Magica to Minecraft (that one is on planetminecraft), then I had the idea to adapt it to Liftoff because Liftoff's editor also works using a coordinate system which is an unobfuscated xml.
  
![coversmall](https://github.com/user-attachments/assets/c8f572f7-7fd8-4d75-9e75-04adf8e1974d)
