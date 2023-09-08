---
description: Functions to validate the entity
---

# Entity validation

### valid

<pre class="language-lua"><code class="lang-lua"><strong>if entity:valid( ) == false then 
</strong>        return
<strong>end
</strong></code></pre>

Entities MUST be checked with player:valid(), otherwise you WILL crash.

Returns true if the player is valid, returns false if the player is invalid.

***

### alive

```lua
if entity:alive( ) == false then 
        return
end
```

Returns true if the player is alive, returns false if the player is not alive.

***

### is\_player

```lua
if entity:is_player( ) == false then 
        return
end
```

Returns true if the entity is a player, returns false if the player is not.

***

### dormant

```lua
if entity:dormant( ) == false then 
        return
end
```

Returns true if the entity is dormant
