# Getting entity variables

## Getting variables of object

Variables of an entity object must be obtained through their relative offset.

These offsets can be obtained through the netvars.get\_offset function, or hardcoded into your code.

***

### get\_int

```lua
local integer_value = entity:get_int(offset)
```

Returns an integer at a given offset.

***

### get\_bool

```lua
local boolean_value = entity:get_bool(offset)
```

Returns a boolean at a given offset.

***

### get\_float

```lua
local floating_point_value = entity:get_float(offset)
```

Returns a floating point at a given offset.

***

### get\_vector

```lua
local vector_value = entity:get_vector(offset)
```

Returns a vector at the given offset.
