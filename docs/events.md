# Events

## Usage

```lua
local fn = function(arg)
    ...
end

callback.new('callback_name', fn)
callback.callback_name(fn) -- the same
```

## List of the events

### Custom events

|Name|Arguments|Description|
|:-|:-|:-|
|`render`|None|Fires every frame. Most functions from the [`render`](/namespaces/render) namespace can only be used here.|
|`pre_move`|cmd: [`UserCmd`](/types/user-cmd)|None|
|`create_move`|cmd: [`UserCmd`](/types/user-cmd)|None|
|`post_move`|cmd: [`UserCmd`](/types/user-cmd)|None|
|`antiaim_setup`|config: [`AntiAimSettings`](/types/anti-aim-settings)|Fires on setting up Anti-aim settings|
|`config_save`|config: [`CheatConfig`](/types/cheat-config)|Fires on any config is saved|
|`config_load`|config: [`CheatConfig`](/types/cheat-config)|Fires on any config is loaded|
|`unload`|None|Fires before script unload|

### Game events
Cheat supports all **[CS:GO events](https://wiki.alliedmods.net/Counter-Strike:_Global_Offensive_Events)**.
Takes the [`Event`](/types/event) in argument

```lua
callback.player_hurt(function(event)
  print(event:get_int('user_id'))
end)
```