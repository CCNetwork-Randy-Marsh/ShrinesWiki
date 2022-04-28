# Configure spawn biomes of Structures

## 1.18.2

Minecraft did some awesome things in the 1.18.2 update. One of these things is the ability to configure the biomes, a 
structure can spawn in. This can be done through data-packs. Fortunately, Shrines provides a global datapack
directory, which applies to all worlds. If you want more customization options, I recommend the usage of https://www.curseforge.com/minecraft/mc-mods/drp-global-datapack.

If you don't know what a datapack is, I recommend reading this article: https://minecraft.fandom.com/wiki/Data_pack

The biomes, a structure can spawn in, are configured through biome tags. Shrines biomes tags are placed into the directory
```data/shrines/tags/worldgen/biome/has_structure```

You can see a list of the available tags to override/merge with here: https://github.com/Silverminer007/Shrines/tree/1.18.2%2B-4.x.x/src/main/resources/data/shrines/tags/worldgen/biome/has_structure

If you would like to see the default values for the tags, you can also use the [data-generator](../devs/datagenerator.md)

Read this article to learn more about tags in general: https://minecraft.fandom.com/wiki/Tag

Here is an example about how to customize structure spawn biomes: [How to make a player house spawn in mountains and stop spawning in deserts](../tutorials/configurePlayerHouseBiomes.md)

## 1.18.1

In 1.18.1 it was quiet simpler to modify biomes. Just open the Structure Config UI and open the structure config of the appropriate structure
and select the biomes you wish.

By default, you can open the structure config UI with `CTRL + K`. This is re-bindable, so take a look at the control settings.

Shrines default structure can be found in the `Included Structures` package.

## 1.16.5

### Shrines-2.0.0 (probably the version you're using)

The only difference you will notice from the 1.18.1 version is the way you open the Config.

Press `k` and expand the top bar through the arrow pointing down in the top right corner. Now Press the `Open Admin Mode` button.

Follow the steps for 1.18.1 now.

### Shrines-1.8.x (if you're still using this version, you should upgrade now)

There is no real comfortable config for structure back here. You can only configure the biomes of custom structures in their config files