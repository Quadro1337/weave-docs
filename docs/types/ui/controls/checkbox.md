# Checkbox

## Description
None

## Examples

```lua
local tab = ui.tab('My tab')
local checkbox = ui.checkbox('My checkbox')
tab:add(checkbox)
tab:register()

callback.render(function()
    print(checkbox:get())
end)
```

## Members

!!! quote "`UICheckbox` is inheriting all members from [`UIControl`](/types/ui/control)"

|Name|Type|Description|
|:-|:-|:-|
|:get(): `boolean`|`function`|None|
|:set(value: `boolean`): `void`|`function`|None|
|:set_callback(callback: `function`): `void`|`function`|None|