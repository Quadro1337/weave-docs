# Texture

## Description
None

## Usage

```lua
local texture = render.create_texture('weave/assets/image.png')
callback.new('render', function()
    render.image(texture, vector(100, 100), vector(200, 200))
end)
```

!!! warning
    [`create_texture`](/namespaces/render#functions) function won't work inside the callbacks. The only way to create `Texture` is create it on the first lines in your script