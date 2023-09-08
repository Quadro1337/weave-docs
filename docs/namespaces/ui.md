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
local tab = ui.tab('My tab')
local checkbox = ui.checkbox('My checkbox')
local nested_checkbox = ui.checkbox('Nested checkbox')
checkbox:add(nested_checkbox)
tab.left:add(checkbox)
tab:register()
```

![Nesting example](/assets/nesting_example.png)

### Config system

```lua
local script_name = 'My script' -- define the script name
script.set_name(script_name) -- set script name
script.set_version('1.1')

local tab = ui.tab(script_name) -- create tab

local checkbox = ui.checkbox('My checkbox') -- create checkbox
checkbox:set(true) -- set true as default value
checkbox:set_key('my_checkbox') -- set key for checkbox

tab.left:add(checkbox) -- add checkbox to tab

tab.left:add(ui.button('Save', function()
    script.save_all('my_script_settings') -- save our checkbox state
    logs.info('\"', script_name, '\"', 'is saved!') -- notify user
end))

tab.left:add(ui.button('Load', function()
    script.load_all('my_script_settings') -- load our checkbox state
    logs.info('\"', script_name, '\"', 'is loaded!') -- notify user
end))

tab:register()
```

## Functions

### Controls
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

### Misc
|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|update|`void`|None|Performs a complete UI update|
|get_accent|[`Color`](/types/color), [`Color`](/types/color)|None|Returns current accent colors|
|override_accent|`void`|color1: [`Color`](/types/color), color2: [`Color`](/types/color)|Overrides accent colors|
|get_menu_position|[`Vector`](/types/vector)|None|Returns current menu position|
|set_menu_position|None|position: [`Vector`](/types/vector)|Sets menu position|
|get_menu_size|[`Vector`](/types/vector)|None|Returns current menu size|
|get_dpi_scale|`number`|None|Returns current DPI scale|