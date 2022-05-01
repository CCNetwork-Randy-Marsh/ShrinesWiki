# Structure Updater

> There is a structure updater for 1.18.1 and 1.18.2, but this article only focuses on the 1.18.2 version

The structure updater was added in Shrines-1.18.2-4.0.0-alpha9. It tries to convert old custom structures to new
configured structure features, structure sets, biome tags and random variation configs. It will also update old random variation
materials to their new format. It also adds all structure where `generate` was set to `false` to the `disabled_structures` config option.
The Structure Updater can be enabled through the `run_structure_updater` config option.
This option is defaulted to true, but will set itself to false after a successful update run. In most cases you won't need to do anything.\
If you want to run the Structure Updater a second time, just set the option to true. It will merge existing files and new files. 
Existing files will be overridden.

## How does the updater work?

> This is not important for the usage of the structure updater and just might be interesting for technical freaks

1. Collect all structure package directories
2. Go over all packages and go over all namespaces
3. Copy the whole namespace to the new `datapacks` directory in the appropriate new data-pack, except from these sub directories:
   - shrines
   - shrines_structures
4. Update all random variation materials to the new encoding
5. Update custom structures (this will also update your custom configurations for shrines default structures)
   1. List all custom structures per namespace
   2. Load all custom structures listed in the previous step
   3. Create new configured structure features, structure sets, biome tags and random variation configs based on the loaded structures
   4. Save the new elements
> The steps in the fifth step will only run if the previous one was fully successful