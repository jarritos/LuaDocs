# Anti freestand resolver

```lua
local eye_angles_offset = netvars.get_offset("DT_CSPlayer", "m_angEyeAngles[0]")

local function normalize_eye_angles(yaw)
    yaw = yaw % 360
    if yaw < 0 then
        yaw = yaw + 360
    end
    return yaw
end

callbacks.register("resolver", function( entry, animdata )
    local realtime = globals.real_time()

    if realtime > entry.first_shot_time + 15 then
        entry.missed_shots = 0;
    end

    local player = entity_list.get_entity( entry.player_index )

    if player:valid( ) == false then 
        return
    end

    local local_player = entity_list.get_entity( entity_list.get_local_index( ) )
    if local_player:valid( ) == false or local_player:alive( ) == false then 
        return
    end
    
    local eye_angles = player:get_vector(eye_angles_offset)

    if entry.missed_shots and realtime >= entry.first_shot_time and realtime < entry.first_shot_time + 15 then
        local missed = entry.missed_shots % 5

        if missed == 0 then
            eye_angles.y = entry.first_shot_yaw
        elseif missed == 1 then
            eye_angles.y = entry.first_shot_yaw + 180;
        elseif missed == 2 then
            eye_angles.y = entry.first_shot_yaw + 90;
        elseif missed == 3 then
            eye_angles.y = entry.first_shot_yaw - 45;
        elseif missed == 4 then
            eye_angles.y = entry.first_shot_yaw + 45;
        end
    else
        local backup_eye_yaw = eye_angles.y;

        local best_damage = 0
        local best_pos = 5
        for i=0, 3 do 
            eye_angles.y = backup_eye_yaw + ( 90 * i );
            eye_angles.y = normalize_eye_angles( eye_angles.y );
            player:set_vector( eye_angles_offset, eye_angles )

            player:animate( )
            player:setupbones( )

            local data = utils.trace_bullet( local_player, player, false, utils.get_local_eye_position( ), player:get_hitbox_position( 0 ), true )
            if best_damage > data.damage then
                best_damage = data.damage
                best_pos = i
            end
        end

        if best_pos ~= 5 then
            eye_angles.y = backup_eye_yaw + ( 90 * best_pos ) + 180;
            eye_angles.y = normalize_eye_angles( eye_angles.y );
        
        else
            eye_angles.y = backup_eye_yaw
        end
    end

    player:set_vector(eye_angles_offset, eye_angles )
end)
```
