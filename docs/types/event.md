# Event

## Description
None

## Usage

```lua
callback.new('player_hurt', function(event)
  print(event:get_int('user_id'))
end)
```

## Members
|Name|Type|Description|
|:-|:-|:-|
|:get_name(): `string`|`function`|None|
|:get_int(key: `string`): `number`|`function`|None|
|:set_int(key: `string`, value: `number`): `void`|`function`|None|
|:get_float(key: `string`): `number`|`function`|None|
|:set_float(key: `string`, value: `number`): `void`|`function`|None|
|:get_string(key: `string`): `string`|`function`|None|
|:set_string(key: `string`, value: `number`): `void`|`function`|None|