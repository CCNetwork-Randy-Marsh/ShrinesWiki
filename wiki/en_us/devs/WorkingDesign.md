## Structural Design of Shrines

> This is an article focused on code specific implementations

> This article only covers the design of Shrines in major version 3.x.x because 2.x.x and 1.x.x were very different

First, we'll take a look at the design of the structure package management. Shrines is designed in stages from
GUI (on the client) to Package Loaders/Package Savers (on the server). The actual GUI marks the actual top, 
which the user is able to see. The GUI relies heavily on the ClientPackageManager. The ClientPackageManager
on exists on the client (that mean there is no client package manager on dedicated servers) and saves the
list of packages that are known in that session. It allows has some useful hooks that affects the GUI. Let's
take a look at the next two stages to better unterstand what the client package manager is for: the server's
version of the ClientPackageManager is the ServerPackageManager. The ServerPackageManager exists one time per session
and handles the structure packages and provides access to the structure packsage to the client. It also makes
sure, that only one client has (write) access to the structure packages. In the case that shrines is running on a
server or local LAN is enabled, we need to sync packages from server to client and back. For that purpose, we have 
the Network(Manager). The ServerPackageManager delegates save tasks to the underlying SaveManager stage, which main
function is to choose in which format the current data is encoded and then select the matching loader to load it.
It also runs the PackageSaver to save the data to disk. Important to note is that all stages can only access their
direct neighbors, in best case only the underlying one. We try to design them as modularised as possible to
allow changes on one stage without changes in another stage (That is better for client-server compatibility).

**For Example:** When the player presses the 'Save' button in the GUI (the top layer) it triggers a function in ClientPackageManager
that collects all packages and send them over the Network to the ServerPackageManager. The ServerPackageManager
verifies the client that requested save against the player that is allowed to edit packages. If the check succeeded
the packages are given to the PackageSaveManager, which gives them to the PackageSaver. The PackageSaver then finally
saves the packages and the message of success goes all the way back up. That sound very complicated and could
probably be solved easier, but this way prevents unintentional access from serverside to client side or unintentional saves
or loads that overrides existing data. We decided to go the 'save' way not the 'easy/fast' way