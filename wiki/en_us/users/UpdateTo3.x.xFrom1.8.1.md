## How to Update Shrines structures mod to version 3.x.x from 1.8.1 (Untested)

Updating shrines structures from 1.8.1 to 2.0.0 doesn't work smoothly, but there are ways for you to prevent these problems. The main problem is that
some structure keys (the name you need to enter for the /locate command) were changed and minecraft tells you all the time that there are structures
missing. You can see that when there are lines in your log 'Missing Structure Start: shrines:high_tempel' or something similar.

You can prevent all these issues if you just create a new world and don't use old worlds anymore, but if you (understandably) don't want to delete all
your worlds you can follow these steps:

1. Fix this for 2.0.0 first
   1. Before Shrines-1.16.5-2.0.0-rc2, you were enforced to run these steps: 
   [update from 1.8.1 to 2.x.x](UpdateTo2.0.0From1.8.1.md)
   2. Since Shrines-1.16.5-2.0.0-rc2 you can just start minecraft one time with 2.0.0 then you're done
      (Shrines runs these steps for you then)
2. Download the latest release from major version 3.x.x and place it in you mods folder
3. Start minecraft and there shouldn't be any problems anymore

Please Note!\
This workaround doesn't work if you have already joined a world (or started a world on a server) 
with 2.x.x or 3.x.x before you used this workaround