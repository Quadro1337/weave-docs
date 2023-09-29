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

|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|text|`void`|font: [`Font`](/types/font), text: `string`, position: [`Vector`](/types/vector)[, color: [`Color`](/types/color), flags: `number`, wrap_width: `number`]|None|
|filled_rect|`void`|mins: [`Vector`](/types/vector), maxs: [`Vector`](/types/vector), color: [`Color`](/types/color)[, rounding: `number`, rounding_flags: `number`]|None|
|image|`void`|texture: [`Texture`](/types/texture), position: [`Vector`](/types/vector)[, size: [`Vector`](/types/vector), color: [`Color`](/types/color), rounding: `number`]|None|

## Misc functions

|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|create_font|[`Font`](/types/font)\|`nil`|path: `string`, size: `number`[, flags: `number`]|:material-alert: Function won't work inside the callbacks. The only way to create [`Font`](/types/font) is create it on the first lines in your script|
|create_texture|[`Texture`](/types/texture)\|`nil`|path: `string`|:material-alert: Function won't work inside the callbacks. The only way to create [`Texture`](/types/texture) is create it on the first lines in your script|
|world_to_screen|[`Vector`](/types/vector)\|`nil`|world_position: [`Vector`](/types/vector)|None|
|get_screen_size|[`Vector`](/types/vector)|None|None|
|text_size|[`Vector`](/types/vector)|font: [`Font`](/types/font), text: `string`[, wrap_width: `number`]|None|