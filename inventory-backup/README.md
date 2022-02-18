# Inventory Backups

** Requires: skript-yaml, skript-gui **

This skript automatically saves a backup of a player's inventory when they die. By default it stores 5 deaths back, but can be configured to whatever you want. The backups are stored in yml files, which by default are in ``plugins/Skript/scripts/inventory-backups/`` but can also be changed.

The skript mainly runs through a GUI accessible through ``/invrestore <player>``. This will show you a history of their backups, starting from most recent, with 5 shown per page. You can do multiple actions by clicking on these backups in various ways. 

A left click will open the backup to you, showing all their items and allowing you to pull specific items out. This will not remove them from the backup, you're simply making a copy of the item. This screen will also show individual buttons for the other actions.

Right clicking will give the backup to the player without clearing their current inventory. If you wish to clear their existing items, you can shift-right-click on the restore button when viewing the backup. 

Shift-left-clicking will teleport you to the location that the player died.

Shift-right-clicking will delete the backup. Be careful.

Some examples and images:

![Main GUI](images/maingui.jpg?raw=true "Main GUI")

![tooltip](images/tooltip.jpg?raw=true "Tooltip Example")

![Viewing a backup](images/backup.jpg?raw=true "Viewing a backup")

---------

I may eventually make a version using vanilla GUIs, but it is highly unlikely as vanilla GUIs are really messy in my opinion