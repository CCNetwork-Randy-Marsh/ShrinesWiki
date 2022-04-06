## Custom Structures(1.16.5-1.8.1; 1.16.5-2.0.0; 1.18.1-3.0.0)

> You might ask why 4.0.0 doesn't have custom structure support anymore. That's just because vanilla allows it now from here out, so no mod is needed for that anymore.

> Technical Info:

Have you always dreamed of a way to add custom structures to the world? With Shrines, now you can! In fact these custom structures can even be shipped with modpacks. However, the exact measure of this feature depends on the version as listed below:

### 1.16.5-1.8.x

Custom structure definition works through a command or you can edit the config files directly. Although, this version isn't recommended  anymore, because it doesn't use the jigsaw structure system and has many (slight) issues. Use the command `/shrines-structures` to add and modify structures (the options should be self explanatory). You can use this [tutorial](https://github.com/Silverminer007/Shrines/wiki/Adding-Custom-Structures) for reference.

### 1.16.5-2.x.x

Custom structure can be edited though a GUI. You can edit the config files easily because they're compressed. You can still ship these custom structures with modpacks. Custom structures are organized in packages, which can be exported/imported to share them with other players. The GUI is quite hidden behind the structure novel UI (Open with 'k' by default). Expand the row on top and press 'Open Admin Mode'. The GUI itself should be self explanatory. Visit our discord if you have any questions

### 1.18.1-3.x.x

3.x.x combined the benefits from version 2.x.x and 1.8.x. Therefore there is a GUI to edit the structure packages. Press CTRL + k by default to open the GUI. The structure (config) files are stored in JSON format. Therefore, they can be edited by hand easily

### 1.18.2-4.x.x

Minecraft added the ability to add own structures (also known as custom structures) via datapacks in 1.18.2. Unfortunately, they don't provide that much customize-ability as Shrines previously did. Shrines aims to add the missing options for example a spawn criteria list that a spawn placement option must fit before a structure can generate. If you're missing any option, just let me know through comments, GitHub issues or on discord. Use shrines:surface or shrines:underground as structure type (the names might change during the development cycle)
