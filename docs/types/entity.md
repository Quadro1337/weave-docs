# Entity

## Description
None

## Usage

```lua
callback.new('create_move', function()
    local me = entity.get(entity.get_local_player())
    if not me then
        return
    end

    print(me:get_prop('DT_CSPlayer', 'm_vecVelocity'))
end)
```

## Members
|Name|Type|Description|
|:-|:-|:-|
|:get_prop(table: `string`, prop: `string`): `any`|`function`|None|