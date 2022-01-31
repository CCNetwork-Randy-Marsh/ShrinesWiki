## How to Update Shrines structures mod to version 2.x.x from 1.8.1 (Untested)

Updating shrines structures from 1.8.1 to 2.0.0 doesn't work smoothly, but there are ways for you to prevent these problems. The main problem is that
some structure keys (the name you need to enter for the /locate command) were changed and minecraft tells you all the time that there are structures
missing. You can see that when there are lines in your log 'Missing Structure Start: shrines:high_tempel' or something similar.

You can prevent all these issues if you just create a new world and don't use old worlds anymore, but if you (understandably) don't want to delete all
your worlds you can follow these steps:

1. Download the latest Shrines structures release from major version 2.x.x and place it in you mods folder
2. Download Compatibility Structures package [here](../../data/Included%20Structures.zip)
3. Extract that archive to your Packets directory inside your shrines-saves directory
   1. Shrines-saves is a directory inside your minecraft directory (where that is depends on your installation)
   2. If that directory doesn't exist, create it
4. Now you should be able to start the game and use shrines structures version 2.x.x without problem

Conclusion:\
That is a very easy solution and shouldn't bring any problems to you, but please note that you shouldn't use this workaround if you don't need to.
That is just because we can't ensure that we will be able to provide that workaround for all future versions. You also won't be able to use the
structure keys, but that shouldn't be a serious problem