# Events

## Usage

```lua
local callback = function(arg)
    ...
end

callback.new('callback_name', callback)
callback.callback_name(callback) -- the same
```

## List of the events

### Custom events

#### `render`
Fires every frame. Most functions from the [`render`](/namespaces/render) namespace can only be used here.

#### `pre_move`
Takes [`UserCmd`](/types/user-cmd) in argument

#### `create_move`
Takes [`UserCmd`](/types/user-cmd) in argument

#### `post_move`
Takes [`UserCmd`](/types/user-cmd) in argument

#### `antiaim_setup`
Fires on setting up Anti-aim settings. Takes [`AntiAimSettings`](/types/anti-aim-settings) in argument

#### `unload`
Fires before script unload.

### Game events
Cheat supports all **[CS:GO events](https://wiki.alliedmods.net/Counter-Strike:_Global_Offensive_Events)**.
Takes the [`Event`](/types/event) in argument

```lua
callback.player_hurt(function(event)
  print(event:get_int('user_id'))
end)
```