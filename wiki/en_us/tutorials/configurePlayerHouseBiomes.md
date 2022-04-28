### How to make a player house spawn in mountains and stop spawning in deserts

> Please read [this](../users/configureBiomes.md) first

As we've learned, we can configure biomes through tags within data-packs. We'll use this option here to customize the biomes, where the player house can spawn.

#### Create a data-pack

This is very simple. First, open the directory where Minecraft stores its files: https://minecraft.fandom.com/wiki/.minecraft

If you have started Minecraft with Shrines already, it created a `datapacks` directory here, otherwise create it yourself.

We'll now add our own data-pack. Just replace `MyDataPack` with a name for your data-pack: \
Create a new directory named `MyDataPack`. Next, we create a new text file called `pack.mcmeta` and fill it with the following:
```json
{
  "pack": {
    "description": "Customization Data-Pack to modify biome tags",
    "pack_format": 9
  }
}
```
As you might have guess, you can write whatever you want into the description. We'll now create a couple of directories, so the following directory structure arises:
`/data/shrines/tags/worldgen/biome/has_structure`.

As we want to modify the biomes for the player house, we create a file called `player_house.json`. See a list of available tags here: https://github.com/Silverminer007/Shrines/tree/1.18.2%2B-4.x.x/src/main/resources/data/shrines/tags/worldgen/biome/has_structure

The default value of this tag looks like this (at the time of 4.0.0-alpha7)
```json
{
  "replace": false,
  "values": [
    "#shrines:is_plains",
    "#minecraft:is_forest",
    "#minecraft:is_taiga",
    "#shrines:is_savanna",
    "#minecraft:is_jungle",
    "#shrines:is_mesa",
    "#shrines:is_icy",
    "#shrines:is_desert",
    "#shrines:is_swamp",
    "#shrines:is_mushroom"
  ]
}
```

If you wanted to add more biomes here for example `#minecraft:is_mountain` (Please note `#` means a tag itself), you
don't need to override the values which improves compatibility with other data-packs. The file could look like this:

```json
{
  "replace": false,
  "values": [
    "#minecraft:is_mountain"
  ]
}
```

If you wanted to remove biomes, you have to override the file, there is no option to remove just a selected amount of biomes.
To remove the desert biomes and add the mountain ones, the file could look like this:

```json
{
  "replace": true,
  "values": [
    "#shrines:is_plains",
    "#minecraft:is_forest",
    "#minecraft:is_taiga",
    "#shrines:is_savanna",
    "#minecraft:is_jungle",
    "#shrines:is_mesa",
    "#shrines:is_icy",
    "#minecraf:is_mountain",
    "#shrines:is_swamp",
    "#shrines:is_mushroom"
  ]
}
```

If you want to add just one single biome, not a whole tag, you can do that too:

```json
{
  "replace": false,
  "values": [
    "minecraft:meadow"
  ]
}
```