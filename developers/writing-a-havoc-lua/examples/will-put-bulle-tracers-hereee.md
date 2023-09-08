# Will put bulle tracers hereee

```lua
health_offset = netvars.get_offset("DT_BasePlayer", "m_iHealth")

callbacks.register("paint", function()
    local player = entity_list.get_entity( entity_list.get_local_index( ) )
    if player:alive( ) == false then 
        return
    end

    local health = player:get_int( health_offset )

    if health < 100 then
        render.filled_rectangle(100, 100, 100, 100, color.new(0, 255, 0))
        render.rectangle(100, 200, 100, 100, color.new(255, 255, 0))
    end
end)
```
