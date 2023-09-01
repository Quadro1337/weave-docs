# Font

## Description
None

## Usage

```lua
local verdana = render.create_font('C:\\Windows\\Fonts\\Verdana.ttf', 14)

callback.new('render', function()
    render.text(verdana, 'Hello world!', vector(100, 100))
end)
```

!!! warning
    [`create_font`](/namespaces/render#functions) function won't work inside the callbacks. The only way to create `Font` is create it on the first lines in your script