# UI

## Description
Functions for work with GUI.

## Examples

### Just checkbox

```lua
local tab = ui.tab('My tab')
local my_checkbox = ui.checkbox('My checkbox')
tab.left:add(my_checkbox)
tab:register()
```

### Customize tab
```lua
local tab = ui.tab('My tab')
tab:set_icon('icon.png')
tab:set_color(color(255, 255, 255), color(0, 0, 0)) -- gradient
tab:register()
```

### Nesting
```lua
local checkbox = ui.checkbox('My checkbox')
local nested_checkbox = ui.checkbox('Nested checkbox')
checkbox:add(nested_checkbox)
```

![Image title](/assets/nesting_example.png)

## Functions
|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|tab|[`UITab`](/types/ui/tab)\|`nil`|label: `string`|Creates tab instance|
|group|[`UIContainer`](/types/ui/container)\|`nil`|label: `string`|Creates group instance|
|checkbox|[`UICheckbox`](/types/ui/controls/checkbox)\|`nil`|label: `string`|None|
|slider|[`UISlider`](/types/ui/controls/slider)\|`nil`|label: `string`, min: `number`, max: `number`|None|
|dropbox|[`UIDropbox`](/types/ui/controls/dropbox)\|`nil`|label: `string`, multiselect: `boolean`, items: `any`[, ...]|None|
|color_picker|[`UIColorPicker`](/types/ui/controls/color-picker)\|`nil`|label: `string`[, alpha: `bool`]|None|
|button|[`UIButton`](/types/ui/controls/button)\|`nil`|label: `string`[, callback: `function`]|None|
|text|[`UINode`](/types/ui/node)\|`nil`|value: `string`[, color: [`Color`](/types/color), bold: `boolean`]|None|
|register_tab|`void`|tab: [`UITab`](/types/ui/tab)|Adds tab to the menu|
|update|`void`|None|Performs a complete UI update|
|override_accent|`void`|color1: [`Color`](/types/color), color2: [`Color`](/types/color)|Overrides accent color|