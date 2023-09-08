# Setting entity variables

## Setting variables of object

Variables of an entity object must be set through their relative offset.

These offsets can be obtained through the netvars.get\_offset function, or hardcoded into your code.

***

### set\_int

```lua
entity:set_int(offset, input_integer)
```

Sets the integer at the given offset to the inputted vector.

***

### set\_bool

```lua
entity:set_bool(offset, input_boolean)
```

Sets the boolean at the given offset to the inputted boolean.

***

### set\_float

```lua
entity:set_float(offset, input_floating_point)
```

Sets the floating point at the given offset to the inputted floating point.

***

### set\_vector

```lua
entity:set_vector(offset, input_vector)
```

Sets the vector at the given offset to the inputted vector.

