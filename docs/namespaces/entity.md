# Entity

## Description
None

## Usage

```lua
local me = entity.get(entity.get_local_player())
```

## Functions
|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|get|[`Entity`](/types/entity)\|`nil`|index: `number`|Returns entity by index|
|get_by_user_id|[`Entity`](/types/entity)\|`nil`|user_id: `number`|Returns entity by user ID|
|get_local_player|`number`|None|Returns local player index|
|get_players|[`Entity`](/types/entity)[]|[enemies_only: `boolean`, include_dormant `boolean`, **callback(player: [`Entity`](/types/entity)): `bool`**: `function`]|All arguments are optional, by default is `false`, `false`, `nil`. If you return `false` in callback this player won't included in the return value|

## Examples

### `get_players`

```lua
callback.new('create_move', function(cmd)
    local players = entity.get_players(false, false, function(player)
        local low_hp = player:get_prop('DT_CSPlayer', 'm_iHealth') < 50
        -- you can do smth else here
        return low_hp
        -- now entity.get_players will only return players with hp lower than 50
    end)

    for _, player in ipairs(players) do
        print('Player health:', player:get_prop('DT_CSPlayer', 'm_iHealth'))
    end
end)
```