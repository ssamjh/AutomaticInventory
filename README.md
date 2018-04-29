# AutomaticInventory

I created this Minecraft server plugin using the Bukkit API to minimize the pain of inventory management.  It automatically sorts player and chest inventories, intelligently deposits player loot into correct containers, and auto-refills hotbar slots when players use the last item in a stack (or break a tool!) but have more of the same in their backpacks.

I stopped working on this project after Minecraft 1.10.  Anyone may use my source code to continue the project, but see the LICENSE file for restrictions.



Deposit ALL your loot into ALL the right boxes with a single slash command!
Plus automatic inventory/chest sorting AND MORE!

![comic](https://s24..cc/ny96ag6r9/comic.png)
![intelligent-inventory-header](https://s24.postimg.cc/xyebj0w39/intelligent_inventory_header.png) 
​
This plugin works very well for Minecraft 1.10, and some earlier versions are available for older versions of Minecraft. However, it will not be updated for future Minecraft versions because I've finally retired from Minecraft development (5 years of plugins!), and I'm moving on to develop indie games. :) You can follow me in my adventures here: 

facebook.com/BigScaryGames
​
Automatic Inventory eliminates tedious inventory management tasks for your players:

/DepositAll finds nearby chests you can access and instantly deposits items from your backpack matching the items in each chest! (Doesn't disturb your hotbar).
Simplifies depositing the correct items into a specific chest to a single click (even from your hot bar).
Automatically sorts personal inventory and chest contents.
Automatically replaces both broken tools and depleted hot bar stacks.
Players may toggle off features they don't like using a slash command Automatic Inventory teaches them about in-game.
AI is a great perk suitable for any server [prison, pvp, factions, survival, skyblock or otherwise] and attractive to every player.
​

**Features**
/DepositAll to instantly dump all your loot into all the right chests. Finds all chests (within one chunk of your location) that you have permission to open and automatically deposits any items from your back pack (not your hotbar) which match items in those chests. Just set up your chests with sample items, and let AutomaticInventory take care of the rest! (Aliases: da, dumpitems, dumploot, depositloot)

Shift-left-click to quickly deposit items into specific chests.
Like /DepositAll, but includes your hotbar items and only matches against items in the specific chest you're opening. Handy for dumping groups of tools or common building blocks from your hotbar into themed chests like "farming", "adventuring", "mining", and "building".

Auto-sorts chests.
When a player opens a chest or chest minecart, the contents will be automatically condensed (restacked) and sorted, grouping similar items together. The first time this happens, the player gets a brief explanation in chat and instructions for disabling the feature if he doesn't like it, and the player also learns that he can make specific chests not auto-sort by renaming them with an anvil (to a name including an asterisk). Players can also avoid sorting a specific chest by sneaking (holding shift) while opening it.

Auto-sorts player inventory.
When a player opens his inventory, it's sorted just like chests above. His hotbar is untouched. Like the chest sort, this can be disabled by any players who don't like it.

Auto-refills hotbars. 
When a player uses the last item in a stack or breaks a tool, a replacement item will leap into his hand from his inventory (assuming a very similar item is available). For example, if a player were to eat the last bread in the bread stack in his hand and there were more bread in his inventory, then the additional bread would jump into the now-empty hot bar slot where the bread he just ate used to be. This applies to weapons, tools, projectiles, blocks, and food.

You may exempt certain items from automatically jumping into the hot bar from inventory in the config file. By default, potions will not. Please leave at least one item (id:0 is air, so that's harmless) in the exemption list, otherwise it will reset to default.

Performant.
Automatic Inventory is light on the CPU, so it won't drag down your server's performance. See this performance report to compare AI against other popular plugins like GriefPrevention, WorldGuard, and NoCheatPlus on an active server with real players (and where all players have all Automatic Inventory's features enabled). If you're unfamiliar with Spigot performance reports, here's the punchline: Automatic Inventory's performance impact is so small, it's hidden by default and you have to click "toggle all hidden" just to find it.

Created by an experienced and professional developer. 
This is a quality plugin that delivers what its description promises. I have a great track record for creating quality plugins and maintaining them over time (see GriefPrevention).

Messages are customizable, even into other languages.
Use Automatic Inventory's messages.yml to translate messages players receive to any other language. The YAML file format isn't always easy to work with, so please make a backup of your messages.yml file before reloading your server with message changes. Also, it helps to use a YAML editor like Notepad++, which can point out syntax errors while you edit.


Note: Some anti-cheat plugins see a player opening a chest from more than a few blocks away and accuse him of "cheating". At the very least, /DepositAll will be limited to a smaller range, and at worst a player might be kicked or banned. To avoid problems, check your anti-cheat plugin's config file and consider relaxing or disabling any right-click reach checks.



**Installation**
Copy AutomaticInventory.jar into your server's plugins folder and then execute the /reload command (or reboot the server).



**Permissions**
By default, all players have all permissions so they have the full feature set. If you want to use this plugin as a donation incentive to monetize your server, you'll have to take away these permissions from the default player group (use your preferred permissions plugin to do that) so that you can selectively restore them to reward players later. If this doesn't fit well with the permission groups you've already got set up, no worries - you have my permission to crack open the JAR (use WinRAR or similar) and change the plugin.yml file to suit your needs. :)

automaticinventory.user.* controls all the permissions below as a group, for your permission-setting convenience.

automaticinventory.sortinventory controls personal inventory sorting.

automaticinventory.sortchests controls chest sorting.

automaticinventory.refillstacks controls auto-replacing broken tools and depleted hot bar stacks.

automaticinventory.quickdeposit controls shift+right-click to quickly deposit matching items into a chest.

automaticinventory.depositall controls access to the /DepositAll command.


**Commands**

/AutoSort chests toggles automatic chest sorting on or off.

/AutoSort inventory toggles automatic personal inventory sorting on or off.

/DepositAll dumps your backpack loot into nearby chests, assuming a chest with very similar items can be found.
