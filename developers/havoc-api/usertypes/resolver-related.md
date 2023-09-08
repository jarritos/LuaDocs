# Resolver related



***

### player\_entry\_t

A collection of fields that can be used for resolving a player.

| Field                       | Type  | Description                                                                                                                                                                  |
| --------------------------- | ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| player\_index               | int   | Player index for obtaining the player object.                                                                                                                                |
| spawntime                   | float | Time at which the player spawned.                                                                                                                                            |
| bot                         | bool  | Flag if the player is a bot.                                                                                                                                                 |
| broke\_lagcompensation      | bool  | Flag if the player is breaking lagcompensation.                                                                                                                              |
| record\_added               | bool  | Flag if the player did not have a record added this tick, usually occuring due to 'defensive dt'.                                                                            |
| new\_commands               | int   | An estimate of the number of new commands the player sent this update.                                                                                                       |
| missed\_shots               | int   | The number of resolver misses on this player.                                                                                                                                |
| first\_miss\_yaw            | float | The yaw shot at originally by the cheat, resets if the cheat shoots at a player 15 seconds after the last shot time.                                                         |
| first\_shot\_time           | float | The time at which the player was shot at last.                                                                                                                               |
| lower\_body\_realign\_timer | float | The time that the player's lower\_body\_yaw\_target will be updated if in the correct conditions. This time is based on the player's tickbase.                               |
| lower\_body\_yaw\_target    | float | The lower body yaw of a player, set to the player's eyeangle when the player is moving OR after 1.1 seconds if they're standing OR 0.22 seconds if they just stopped moving. |
| last\_recieved\_tick        | int   | The last tick the player sent a command to the server.                                                                                                                       |

***

#### get\_previous\_anim\_data

```lua
local previous_data = entry:get_previous_anim_data()
```

Returns the previous anim data in form of animation\_data\_t

***

### animation\_data\_t

A collection of fields that describe a players animation state

| Field                 | Type                    | Description                                    |
| --------------------- | ----------------------- | ---------------------------------------------- |
| velocity              | vector                  | Velocity of player, with accuracy adjustments. |
| origin                | vector                  | Player position in map.                        |
| mins                  | vector                  | Player's collision mins.                       |
| maxs                  | vector                  | Player's collision maxs.                       |
| weapon                | pointer                 | Pointer to player's weapon.                    |
| anim\_layers          | array of anim\_layer\_t | Array of animation layers.                     |
| flags                 | int                     | Player flags, directly from m\_fFlags netvar   |
| simulation\_time      | float                   | Player's tickbase converted into time form.    |
| old\_simulation\_time | float                   | Old simulation time last update.               |
| duck\_amount          | float                   | Duck amount, \[0.f-1.f]                        |



***
