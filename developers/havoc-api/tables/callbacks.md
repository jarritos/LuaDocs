---
description: All cheat related events you can listen to with a callback
---

# Callbacks

***

### paint

{% code overflow="wrap" lineNumbers="true" %}
```lua
callbacks.register("paint", function)
```
{% endcode %}

Fired every time a frame is rendered, Render functions should be called on this event.

***

### resolver

{% code overflow="wrap" lineNumbers="true" %}
```lua
callbacks.register("resolver", function(entry, animdata)

end)
```
{% endcode %}

Fired every time the game runs a command (usually up to 64 times a second, equal to tickrate) while you're alive. This is the best event for processing data that only changes when the game receives an update from the server, like information about other players.&#x20;

(NOTE: will not be ran if the player's yaw is able to be resolved through m\_flLowerBodyYawTarget)

<table><thead><tr><th>Type</th><th data-hidden>Arguments</th><th data-hidden>Desc</th></tr></thead><tbody><tr><td>player_entry_t</td><td>entry</td><td>A collection of fields that can be used for resolving a player.</td></tr><tr><td>anim_data_t</td><td>animdata</td><td>A collection of fields that describe a players animation state</td></tr></tbody></table>

***
