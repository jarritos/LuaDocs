# Other



### animate

```lua
player:animate()
```

Runs the animation system on the player object.

NOTE: must be a PLAYER object

***

### setupbones

```lua
player:setupbones()
```

Runs setupbones on the player object, m\_CachedBoneData is the matrix being set up.

NOTE: this will NOT affect the player's visual bone matrix.

***

### get\_hitbox\_position

<pre class="language-lua"><code class="lang-lua"><strong>local head_hitbox = player:get_hitbox_position(HITBOX_HEAD)
</strong></code></pre>

Returns the center position of the given hitbox in form of vector.

Hitbox indexes can be found below:

```
HITBOX_INVALID = -1, 
HITBOX_HEAD = 0
HITBOX_NECK = 1
HITBOX_PELVIS = 2
HITBOX_STOMACH = 3
HITBOX_LOWER_CHEST = 4
HITBOX_CHEST = 5
HITBOX_UPPER_CHEST = 6
HITBOX_RIGHT_THIGH = 7
HITBOX_LEFT_THIGH = 8
HITBOX_RIGHT_CALF = 9
HITBOX_LEFT_CALF = 10
HITBOX_RIGHT_FOOT = 11
HITBOX_LEFT_FOOT = 12
HITBOX_RIGHT_HAND = 13
HITBOX_LEFT_HAND = 14
HITBOX_RIGHT_UPPER_ARM = 15
HITBOX_RIGHT_FOREARM = 16
HITBOX_LEFT_UPPER_ARM = 17
HITBOX_LEFT_FOREARM = 18
HITBOX_MAX = 19
```

***

### get\_layer\_sequence\_activity

```lua
local sequence_activity = player:get_layer_sequence_activity(layer_index)
```

Returns the sequence activity of the indexed layer.
