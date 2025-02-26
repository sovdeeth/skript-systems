# NBT Player Data
Basic NBT-based player data system.
Stores strings and numbers in NBT, but accessible via variables.

Example:
{-npd::%player%::strength} = 1
This value is stored in npd_data/<player's uuid>.dat as {strength: 1}.
All values under {-npd::%player%::...} are stored in the file.

Use npd_load_player_data() to load data into variables.
The save function saves data to nbt.
The unload function saves data and clears the variables.

By default, data is loaded when the player joins, saved every five minutes, and unloaded when they quit.

A default nbt file can be provided that all new users' values will be set to.

### NOTE: ONLY STRINGS AND NUMBERS WILL BE STORED. NO COMPLEX TYPES (yet).
