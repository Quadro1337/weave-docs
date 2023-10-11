# Render

## Description
None

## Usage

```lua
callback.render(function()
    render.filled_rect(vector(100, 100), vector(200, 200), color(255, 255, 255))
end)
```

## Draw functions

!!! warning "These functions won't work outside the [`render`](/events#render) callback"

|Function name|Arguments|
|:-|:-|
|line|pos1: [`Vector`](/types/vector), pos2: [`Vector`](/types/vector), color: [`Color`](/types/color)[, thickness: `number`]|
|filled_rect|mins: [`Vector`](/types/vector), maxs: [`Vector`](/types/vector), color: [`Color`](/types/color)[, rounding: `number`, rounding_flags: `number`]|
|rect|mins: [`Vector`](/types/vector), maxs: [`Vector`](/types/vector), color: [`Color`](/types/color)[, thickness: `number`, rounding: `number`, rounding_flags: `number`]|
|filled_circle|position: [`Vector`](/types/vector), radius: `number`, color: [`Color`](/types/color)[, segments: `number`]|
|circle|position: [`Vector`](/types/vector), radius: `number`, color: [`Color`](/types/color)[thickness: `number`, segments: `number`]|
|vertical_gradient|mins: [`Vector`](/types/vector), maxs: [`Vector`](/types/vector), color_top: [`Color`](/types/color), color_bottom: [`Color`](/types/color)[, rounding: `number`, rounding_flags: `number`]|
|horizontal_gradient|mins: [`Vector`](/types/vector), maxs: [`Vector`](/types/vector), color_left: [`Color`](/types/color), color_right: [`Color`](/types/color)[, rounding: `number`, rounding_flags: `number`]|
|filled_arc|position: [`Vector`](/types/vector), radius: `number`, angle_min: `number`, angle_max: `number`, color: [`Color`](/types/color)[, segments: `number`]|
|arc|position: [`Vector`](/types/vector), radius: `number`, angle_min: `number`, angle_max: `number`, color: [`Color`](/types/color)[thickness: `number`, segments: `number`]|
|text|font: [`Font`](/types/font), text: `string`, position: [`Vector`](/types/vector)[, color: [`Color`](/types/color), flags: `number`, wrap_width: `number`]|
|image|texture: [`Texture`](/types/texture), position: [`Vector`](/types/vector)[, size: [`Vector`](/types/vector), color: [`Color`](/types/color), rounding: `number`]|

## Misc functions

|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|create_font|[`Font`](/types/font)\|`nil`|path: `string`, size: `number`[, flags: `number`]|:material-alert: Function won't work inside the callbacks. The only way to create [`Font`](/types/font) is create it on the first lines in your script|
|create_texture|[`Texture`](/types/texture)\|`nil`|path: `string`|:material-alert: Function won't work inside the callbacks. The only way to create [`Texture`](/types/texture) is create it on the first lines in your script|
|world_to_screen|[`Vector`](/types/vector)\|`nil`|world_position: [`Vector`](/types/vector)|None|
|get_screen_size|[`Vector`](/types/vector)|None|None|
|text_size|[`Vector`](/types/vector)|font: [`Font`](/types/font), text: `string`[, wrap_width: `number`]|None|