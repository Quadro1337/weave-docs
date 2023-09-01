# Script

## Description
Here you can serialize and deserialize all [`UIControl`](/types/ui/control) states. Serialization and deserialization become available when **keys** are set up. You can read more about settings up keys **[here](/types/ui/control/#keys)**

## How it's works
As you may know Weave is saving cheat settings on the servers. But all script's configuration files are located in the folder `weave/settings/%script_name%/`. This is temporary solution.

## Example

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
    log.info('\"', script_name, '\"', 'is saved!') -- notify user
end))

tab.left:add(ui.button('Load', function()
    script.load_all('my_script_settings') -- load our checkbox state
    log.info('\"', script_name, '\"', 'is loaded!') -- notify user
end))

ui.register_tab(tab)
```

## Configuration

!!! warning "You have to setup `UIControl` [keys](/types/ui/control/#keys) before save or load"

|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|save|`void`|name: `string`, items: [`UIControl`](/types/ui/control)[, ...]|Saves the passed [`UIControl`](/types/ui/control) states|
|save_all|`void`|name: `string`|Saves the all [`UIControl`](/types/ui/control) states|
|dump_base64|`string`\|`nil` if failure|items: [`UIControl`](/types/ui/control)[, ...]|Return the passed [`UIControl`](/types/ui/control) states from base64 string|
|dump_all_base64|`string`\|`nil`|None|Return the all [`UIControl`](/types/ui/control) states encoded in base64|
|load|`void`|name: `string`, items: [`UIControl`](/types/ui/control)[, ...]|Loads the passed [`UIControl`](/types/ui/control) states|
|load_all|`void`|name: `string`|Loads the all [`UIControl`](/types/ui/control) states|
|load_base64|`void`|text: `string`, items: [`UIControl`](/types/ui/control)[, ...]|Loads the passed [`UIControl`](/types/ui/control) states from base64 string|
|load_all_base64|`void`|text: `string`|Loads the all [`UIControl`](/types/ui/control) states encoded in base64|
|set_name|`void`|name: `string`|Overrides script name|
|set_version|`void`|version: `string`|By default is `1.0`. The version will be written into each saved configuration. You can override this value if you want to remove backward compatibility with older configurations|