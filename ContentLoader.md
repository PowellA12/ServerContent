# Raindrop #
The purpose of this file is to give an explaination of each functionality of the content loader that exists within Almura.  Through out the history of Almura there has been a 3 different versions in which we implemented the content loader.  The first version was on the Spoutcraft platform.  The second implemenation was within the Minecraft 1.7.10 environment running on top of Cauldron.  The third implementation was build upon Minecraft 1.12.2 and SpongeForge.

The current base directory structure is:
* `2.5` - Almura 2.5 Rediscovered
* `3.0` - Almura 3.0 Resurrected

**The information below is only related for the 3.0 version as previous implementations have been abandoned.**

Blocks and Items are constructed from a various combination of basic files.
The files for the content loader go within `(BaseMinecraftDirectory)/assets`
* BlockState:   `/fs/assets/almura/blockstates/`
* Content:      `fs/assets/almura/content/`
* Models:       `/fs/assets/almura/models/`
* Texture:      `/fs/assets/almura/textures/`

## Blockstates
Blockstate files hold various types of information which includes things such as forge markers, model, transform, variants and rotation specifications.
Each subdirectory under `blockstates` represents a implementation type.
* `cache` - storage caches
* `crop` - custom crops
* `horizontal` - blocks in which have special render properties
* `leaf` - leaves for custom trees
* `log` - logs for custom trees
* `normal` - normal 1x1x1 blocks
* `sapling` - custom tree saplings
* `slab` - slabs
* `stair` - stairs
* `storage` - storage crates and boxes

## Content
The content directory is broken up slightly different than how Blockstates are.  The following subfolders exist:
* `block` - core directory for all block type implementations
* `block_sound_group` - custom sounds are stored here
* `generation` - specification files for world generation are stored here
* `grass` - DON'T KNOW
* `item` - item specification
* `item_group` - Creative Tab setup files
* `tree` - custom tree implemenation files

## Models
The models directory contains both `.OBJ` and `.JSON` based model definitions.  The location of these files are important to only `block` and `item`.  Past the base directories you only need to make sure that the content files point to the appropriate subfolders past each parent directory.  Note:  OBJ models require the usage of a `.MTL` file to load the information about the `.OBJ` mode.
* `block` -
* `item` -

## Textures
The textures directory contains images for not only the content loader but the base Almura code implementation itself.  The following directories exist:
* `accessories` - cutout images for accessories feature.
* `backgrounds` - individual background images for MainMenu.
* `block` - Block textures can be on a sprite sheet.
* `item` - Item textures **cannot be** on a sprite sheet.
