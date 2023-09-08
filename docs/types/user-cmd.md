# UserCmd

## Description
None

## Usage

```lua
callback.create_move(function(cmd)
    print(cmd.command_number)
end)
```

!!! abstract "Important"
    The user cmd only passed in [`pre_move`](/events/#pre_move), [`create_move`](/events/#create_move), [`post_move`](/events/#post_move) events

## Members
|Name|Type|Description|
|:-|:-|:-|
|command_number|`number`|None|
|tick_count|`number`|None|
|view_angles|[`Vector`](/types/vector)|None|
|aim_direction|[`Vector`](/types/vector)|None|
|move|[`Vector`](/types/vector)|None|
|buttons|`number`|None|
|send_packet|`boolean`|None|