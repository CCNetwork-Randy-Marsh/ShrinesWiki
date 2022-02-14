## How to Update Shrines structures mod to version 2.x.x from 1.8.1

> If you want to use an outdated version for some reason, you might want to follow these steps: 
> [Update to Shrines 2.0.0-rc1 or lower](outdated/UpdateTo2.0.0From1.8.1.md)

On most recent version, the update won't cause any issue in most cases. If you haven't used custom structures yet,
you only need to download the most recent version of Shrines for 1.16.5 (the ones with major version 2 (2.x.x))
and place it in your mods folder. Remember to delete the old file. If you want to keep your configurations from
the old version, you need to use at least version 2.1.0.

### Import legacy custom structures

If you have used custom structures before, it depends on the size of your structures what you will need to do.
If all your structures have only one structure template (previously known as .nbt files), you're done with starting the game,
open the structure config UI (Press k by default) and then press 'Import Legacy Packet'. To import the old
custom structures, you need to select the shrines-saves directory and then confirm. Restart Minecraft and you're done.
If your structure are huger, you'll need to do some things yourself afterwards. 

### Structure generation system change

The structure generation system
was changed to jigsaw in the major update, which means that there are pools of structure templates that are used
to generate more dynamic structures like Minecraft's villages. Shrines isn't able to update structures that were
huger than 48x48x48 blocks before, so you will need to update that yourself. You need to be familiar with the jigsaw
system in advance, so I recommend doing some research. You need to set the start pool of a structure in it's
configuration, you need to add the structure templates in its UI and you need to create the structure template
pools in its UI to update the old structures.

If you need help, feel free to ask on discord or open an issue on GitHub

[![Discord](https://img.shields.io/discord/777129358769782814?label=discord)](https://discord.gg/8pUpWCEUe2)
[![GitHub issues](https://img.shields.io/github/issues/Silverminer007/Shrines)](https://github.com/Silverminer007/Shrines/issues)