## Target of Shrines Structures development

Shrines Structures isn't nearly done with development. Here I want to show some targets of development.

Currently, the user is enforced to create their structure packages in the shrines-saves directory. 
The mods loads the structure configuration files manually, as soon as the game starts. Afterwards, it iterates
over all found elements and registers these to Minecraft's static registry. Unlike Biomes, which can be 
added/configured/removed via JSON Data-packs, because that's a dynamic registry, 
structures meanwhile structure configs are statically registered. Unfortunately, static registry 
are only open as soon as the game starts, but data packs, on the one hand are first time available when 
the loading screen shows up, that's too late. On the other hands data-packs can be reloaded and static registries
can't. For that reason it's enforced to have all structures in shrines-saves. For the future it's planned to
break this limitation and make structures registry dynamic in which way ever. That would have several
advantages: First, the data/structure packs can be at more different places. Secondly, other mods can add new
structures easily trough soft dependencies in their own, shipped data packs. Third benefit is that it is possible to
exchange structures during runtime, without the need of restarting minecraft all the time.

A side effect of that change, is that the GUI will be removed. We can't maintain a GUI that does not know where
the actual data is. In case that data packs are compressed ZIP data packs we would we entirely impossible to make any
change there because we would have to decompress and compress them all the time. An alternative system for Graphical
structure definition is another java application that generates the packages based on the user's inputs, but
we haven't made a final decision on this. We need to evaluate how much effort this is worth, because creating structure
configuration should be much harder that creating other data pack components. The knowledge of JSON file creation
and schemata is the smallest requirement for minecraft data packs

In case that feature applies well, we'll split things up into two mods: 'Dynamic Structures' and 'Shrines Structures'.
First one is going to be the library mod which handels all stuff related to structure registration, random variation
and data pack structure definition/loading and the second adds the actual structures and special features like the
structure novels.