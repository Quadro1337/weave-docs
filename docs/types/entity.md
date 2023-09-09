# Entity

## Description
None

## Usage

```lua
callback.create_move(function()
    local me = entity.get(entity.get_local_player())
    if not me then
        return
    end

    print(me:get_prop('DT_CSPlayer', 'm_iHealth'))
end)
```

## Members
|Name|Type|Description|
|:-|:-|:-|
|:get_prop(table: `string`, prop: `string`): `any`|`function`|None|
|:get_origin(): [`Vector`](/types/vector)|`function`|None|
|:get_velocity(): [`Vector`](/types/vector)|`function`|None|