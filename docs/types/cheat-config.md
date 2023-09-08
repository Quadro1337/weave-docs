# CheatConfig

## Description
`CheatConfig` is an abstraction that contain information about configuration.

## Usage

```lua
callback.config_save(function(config)
    print(config.name, config.id)
end)
```

## Members
|Name|Type|Description|
|:-|:-|:-|
|name|`string`|None|
|id|`string`|Unique ID of config|
|author|`string`|The name of the user who created this config|
|last_update_by|`string`|The name of the user who was edited this config last time|
|private|`boolean`|None|