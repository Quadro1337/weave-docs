# Anti-aim settings

## Description
None

## Usage

```lua
callback.antiaim_setup(function(settings)
    settings.jitter_angle = 15
end)
```

## Members
|Name|Type|Description|
|:-|:-|:-|
|id|`number`|ID of current config|
|side|`number`|Current side of the desync, `-1` or `1`|
|force_off|`boolean`|None|
|pitch|`number`|None|
|ignore_freestand|`boolean`|None|
|ignore_manuals|`boolean`|None|
|yaw_add|`number`|None|
|spin|`boolean`|None|
|spin_speed|`number`|None|
|spin_range|`number`|None|
|jitter_angle|`number`|None|
|align_desync|`boolean`|None|
|randomize_jitter|`boolean`|None|
|desync_amount|`number`|None|
|desync_jitter|`boolean`|None|
|desync_direction|`number`|None|
|align_by_target|`number`|None|
|inverter|`boolean`|None|