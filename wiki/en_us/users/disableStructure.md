# Disable Structures

## 1.18.2

> This requires 4.0.0-alpha8 or above

In 1.18.2, the option to disable structure moved to shrines config. The required file is in the following directory relative to
your [minecraft installation directory](https://minecraft.fandom.com/wiki/.minecraft): `config/shrines/settings.toml`.\
This file is generated the first you start minecraft with Shrines installed. In this file, you will find a line like this:
```toml
disabled_structure = []
```
Add all structure ids, which you would like to disable, separated by `,`. For example, this could look like this:
```toml
disabled_structure = ["shrines:balloon", "shrines:tall_player_house", "shrines:small_player_house"]
```
This line disables the balloon and both versions of the player house. Please note that you're still able to find 
already generated structures.\
You can even disable vanilla structures or structures of other mods:
```toml
disabled_structure = ["minecraft:mineshaft", "minecraft:mansion", "minecraft:ruined_portal_desert"]
```
You can leave out the `minecraft:` in theory, but I kept it here for clarity. You can even disable whole structure tags. That would look like this:
```toml
disabled_structure = ["#minecraft:village", "#minecraft:mineshaft", "#minecraft:ruined_portal"]
```
You can combine tags and regular entries as desired.

## 1.18.1 and before

In 1.18.1 and before, there was a simple config option for each structure. Set the option `generate` to `false` 
and the structure won't spawn anymore. It isn't possible to disable non-Shrines structures (you can still disable custom structures)