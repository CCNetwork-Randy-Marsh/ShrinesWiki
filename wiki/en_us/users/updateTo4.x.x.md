### Update to Shrines 4.x.x / Minecraft 1.18.2

> This article is untested right now

> This only works with alpha 6 or above

Minecraft changed many internals concerning structures in 1.18.2. We're now able to add custom structures without mods!
Unfortunately, Mojang missed a few important options for customisation, which Shrines aims to ship, but that's out of the scope
of this tutorial. In this tutorial, we will focus on how you can continue your old world with the new version of shrines.

**Before you continue, create a backup of your world, in best case of your whole minecraft directory**

If you haven't used custom structures before, you should already be good to go. Just make sure you have Shrines-4.0.0-alpha6 or above installed.
Even if this system seems to be stable, issues can still appear, so remember to create a backup! You might experience some issues
with the `/locate` command like `shrines:nether_shrine` points to a `shrines:nether_shrine_nether`, because they were one structure before,
but you don't need to worry about chunk regeneration or crashes anymore (Please keep in mind that this system is still not 100% secure,
don't delete your backup immediately).

If you have used custom structures before, you'll have to do some manual work. You can either add all structure IDs
to shrines removed_structures in `minecraft/config/shrines/settings.toml`, or you add a new configured structure feature for 
each structure ID. If you add the structure IDs to the removed_structures option (We'll refer to these structures as removed structures),
they will be grouped to a single `shrines:deleted_structure`. That step can't be reverted.
If you decide to re-create the custom structures in 1.18.2 (a tutorial for that will follow), you must take care about the names of
your configured structure features. They must match the old structure IDs