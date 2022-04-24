## Random variation (1.16.5-2.x.x; 1.18.1-3.x.x; Future 1.18.2-4.x.x releases (not yet)

There are many structures that can also have variant materials. E.g. the Watchtower is built from spruce, but a dark oak watchtower could be naturally generated as a new, fresh alternative. Shrines' Random variation feature exchanges the materials of its builds on every placement. You can see a Balloon in white, in red, purple, green etc.
Since 3.x.x you're also able to fully configure random variation through datapacks.
![](https://media.forgecdn.net/attachments/422/138/random_variation_11012022.png)


## How to customize random variation

> This paragraphs requires some basic knowledge about minecraft datapacks
> 
> This covers only how random variation works in Shrines most recent versions

Let's first talk about how random variation works. Here is what we want to achieve with it:

Imagine the [] being one block each. We will use 2-dimensional only.

Imagine you want this structure:

```
[stone_bricks] [stone_bricks] [acacia_planks] [stone_brick_stairs]
[acacia_slab] [oak_slab] [stone_brick_slab] [torch]
[stone_bricks] [stone_bricks] [acacia_planks] [stone_brick_stairs]
```

to look like this one:

```
[mossy_stone_bricks] [mossy_stone_bricks] [spruce_planks] [mossy_stone_brick_stairs]
[spruce_slab] [dark_oak_slab] [stone_brick_slab] [torch]
[mossy_stone_bricks] [mossy_stone_bricks] [mossy_stone_bricks] [mossy_stone_brick_stairs]
```

but because you're lazy, you only want to write

```
stone_bricks -> mossy_stone_bricks
acacia -> spruce
oak -> dark_oak
```

In fact, random variation allows you to do that. You don't even need to generate new structure files in advance, the mod will do
that at generation time. You still need to help Shrines a bit. It doesn't know which blocks belong to which "material".

A "material" is a set of blocks assigned to an "element id". For example the acacia material looks like this:

```
acacia
    acacia planks -> planks
    acacia slabs -> slab
    acacia stairs -> stairs
    acacia log -> log
```

and the oak material look like this:

```
oak
    oak planks -> planks
    oak slabs -> slab
    oak stairs -> stairs
    oak log -> log
```

(In fact, both materials contain more blocks, but they aren't important for this article)

You probably noticed already the common ground of both materials. The mod will go over each block of the structure
and checks which block of the material it matches and takes the assigned id. Next, it will look at the assigned materials
and search for the id and take the block. The taken block will be placed then

That's how it works in a bit simplified. To make random variation work properly, you need at least 3 files. 1 "random variation config"
file and 2 "random variation material" file. You can add those files though datapacks. Just as minecrafts datapack entries,
they have to be placed into a certain directory. Ass directories are relative to the datapack's namespace.

Path for random variation config: `shrines/random_variation/config`

Path for random variation material: `shrines/random_variation/material`

Here is an example config file: https://github.com/Silverminer007/Shrines/blob/1.18.2%2B-4.x.x/src/main/resources/data/shrines/shrines/random_variation/config/azalea_pavilion.json

Here is an example material file: https://github.com/Silverminer007/Shrines/blob/1.18.2%2B-4.x.x/src/main/resources/data/shrines/shrines/random_variation/material/acacia.json

There are 53 default material files that you can use, so our example could easily be implemented in a config file:

```
{
  "remaps": [
    [
      {
        "first": "shrines:stone_bricks",
        "second": "shrines:mossy_stone_bricks"
      },
      {
        "first": "shrines:acacia",
        "second": "shrines:spruce"
      },
      {
        "first": "shrines:oak",
        "second": "shrines:dark_oak"
      }
    ]
  ]
}
```

**Important: The name of your config file must be the same as the configured structure feature. Same for namespace**

If you have questions or concerns feel free to ask on discord: https://discord.gg/8pUpWCEUe2

[Home](Home.md)