
## Parse Location from Command Input.
#### Provides functions to allow Minecraft-like coordinates in commands (^ and ~)


To use, add text arguments to your command to capture the coordinates.
Feed these arguments into the locationFromCommandInput function, 
along with an origin location (usually the sender's location).
The function will return the origin location modified by the inputs.
This follows typical Minecraft command coordinates, which can be read about on the wiki:
https://minecraft.wiki/w/Coordinates#Commands


You do not need to supply all 3 coordinates, the function will work fine if one or more are not set.
You can also use numbers as inputs. 12 will be treated the same as "12".
Finally, you can also mix and match normal coords, ~, and ^. Just remember they're applied in xyz order.


Advanced users may want to use the parsed coordinates on their own. 
Please see the parseCoordinate() and applyParsedCoordinate() functions for that purpose.


Examples of use:
```
command /teleport-me <x:text> <y:text> <z:text>:
    executable by: player
    trigger:
        teleport player to locationFromCommandInput({_x}, {_y}, {_z}, player)
```