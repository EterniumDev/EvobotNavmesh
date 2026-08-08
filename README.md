# EvobotNavmesh
 Repository for Natural Selection - Evobot navmesh and bin files
The nav files are used in the Evobot NS addon and are used in Recast to pathfind around the level

The bin files are used by the GoldSrcNavEditor, modified by github/RGreenlees



# Contribution

Navmeshes created by Eternium and RGreenlees

Please if you're contributing your own navmeshes don't replace my navmeshes in the repo just create a subfolder or use a version number

Also make sure to include both the bin files and nav files (for the same version) to ensure others can improve your navmeshes in the future


# Making your own navmeshes

Download the following files into one folder (from this repo)
DroidSans.ttf
GoldSrcNavEditor.exe
navtool.cfg
SDL2.dll

Move a BSP file that you want to edit into the same folder

Run GoldSrcNavEditor.exe

Click input, choose map (select your bsp file)

Click build at the bottom right, wait for it to build the blue navmesh

Click Save and export (always both of these), the .bin file is only usable by the editor and the .nav file is only usable by the addon, always keep both so you can iterate on your navmesh

Hold right click and use WASD to move around in the 3d space, find areas that are vents and link them using off-mesh links
Add a WALL CLIMB for skulks to climb a wall up and a DROP for skulks or others to drop out of the vents

for example on ns_eclipse the railings in marine start are considered transparent in the editor
This means that the AI will try to walk through them (unsuccessfully) use the Edit Map Collision with SOLID SURFACE to change these into solid walls

some areas will also show solid when they shouldnt be like Vines or Bushes that players can actually walk through, change these to ILLUSIONARY

Ensure you change the walls where ladders are to LADDER and add both ladder and wall climb and drop offmesh linkes adjacent to them

add offmesh links for Ladder ontop of and below a ladder

## Testing your own navmeshes

you'll frequently need to test the evobots in game to determine if your navmesh allows them to freely navigate the map

in game use the commands

`evobot addbot`
`evobot addbot`
`evobot debug drone`
`cometome`

this will make the evobots walk to your current position every time you type `cometome` in the console

test out vents, general access for all hive locations, RTs and marine start

## Maps completed
ns_veil

ns_deathsiege_v4

ns_crude_b3

ns_ayumi_e_b5

ns_machina

ns_hera

ns_eclipse

ns_caged

ns_eon

ns_delta

ns_block_v2a



## Work in progress
ns_agora

ns_11th_hr121

ns_askr_a2

ns_ayumi

ns_altair

ns_green_b1

ns_lucid

ns_sechala

ns_orbital

ns_nothing_classic

ns_lost


## Navmeshes needed

ns_dust2

ns_psixnighthunt_v01

ns_ragnarok (no bin and nav file is buggy)

ns_shiva (no bin file)



