# Script

## Description
Here you can serialize and deserialize all [`UIControl`](/types/ui/control) states. Serialization and deserialization become available when **keys** are set up. You can read more about settings up keys **[here](/types/ui/control/#keys)**

## How it's works
As you may know Weave is saving cheat settings on the servers. But all script's configuration files are located in the folder `weave/settings/%script_name%/`. This is temporary solution.

## Example

Example can be found **[here](/namespaces/ui/#config-system)**

## Configuration
All functions return `string`|`nil`, text of error or `nil` if there's no error. 
!!! warning "You have to setup `UIControl` [keys](/types/ui/control/#keys) before save or load"

|Function name|Return value|Arguments|Description|
|:-|:-|:-|:-|
|save|`string`\|`nil`|name: `string`, items: [`UIControl`](/types/ui/control)[, ...]|Saves the passed [`UIControl`](/types/ui/control) states|
|save_all|`string`\|`nil`|name: `string`|Saves the all [`UIControl`](/types/ui/control) states|
|dump_base64|`string`\|`nil`, `string`\|`nil`|items: [`UIControl`](/types/ui/control)[, ...]|Return the passed [`UIControl`](/types/ui/control) states from base64 string|
|dump_all_base64|`string`\|`nil`, `string`\|`nil`|None|Return the all [`UIControl`](/types/ui/control) states encoded in base64|
|load|`string`\|`nil`|name: `string`, items: [`UIControl`](/types/ui/control)[, ...]|Loads the passed [`UIControl`](/types/ui/control) states|
|load_all|`string`\|`nil`|name: `string`|Loads the all [`UIControl`](/types/ui/control) states|
|load_base64|`string`\|`nil`|text: `string`, items: [`UIControl`](/types/ui/control)[, ...]|Loads the passed [`UIControl`](/types/ui/control) states from base64 string|
|load_all_base64|`string`\|`nil`|text: `string`|Loads the all [`UIControl`](/types/ui/control) states encoded in base64|
|set_name|`void`|name: `string`|Overrides script name|
|set_version|`void`|version: `string`|By default is `1.0`. The version will be written into each saved configuration. You can override this value if you want to remove backward compatibility with older configurations|