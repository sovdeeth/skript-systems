# Inventory Backups

**Requires: SkBee (tested on 2.8.2+, should work on 2.5.0+), skript-gui 1.3+**

This skript automatically saves a backup of a player's inventory when they die. By default it stores deaths for 30 days, but can be configured to whatever you want. The backups are stored in NBT files, which by default are in ``plugins/inventory-backups/`` but can also be changed.

The skript mainly runs through a GUI accessible through ``/invrestore <player>``. This will show you a history of their backups, starting from most recent, with 5 shown per page. You can do multiple actions by clicking on these backups in various ways. 

A left click will open the backup to you, showing all their items and allowing you to pull specific items out or add items in. These changes do not affect the backup until you click the "save edits" button. This screen will also show individual buttons for the other actions.

Right clicking will give the backup to the player without clearing their current inventory. If their inventory is full, the rest of the items will drop on the ground at the player. If you wish to clear their existing items, you can shift-click on the restore button when viewing the backup.

Shift-left-clicking will teleport you to the location that the player died.

Shift-right-clicking will delete the backup. Be careful.

Some examples and images:

![Main GUI](images/maingui.jpg?raw=true "Main GUI")

![Restoring a backup](images/restore.jpg?raw=true "Restoration Tooltip")

![Viewing a backup](images/backup.jpg?raw=true "Viewing a backup")

---------

I may eventually make a version using vanilla GUIs, but that's so much more effort and so much messier
