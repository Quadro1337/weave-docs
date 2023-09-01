# Control

## Description
`UIControl` is an abstraction containing functions for working with its state. There's the several instances of `UIControl`. You can see more details **[here](/types/ui/controls)**

## Members

!!! quote "`UIControl` is inheriting all members from [`UINode`](/types/ui/node)"

|Name|Type|Description|
|:-|:-|:-|
|:set_key(key: `string`): `void`|`function`|None|
|:get_key(): `string`|`function`|None|

## Keys
A **key** is a unique value. You should set the **key** value manually if you desired to use built-in config for your script. If you don't need this functionality, you can ignore the **keys**.

!!! info "If you want to prevent saving some `UIControl` value, you should set key to `nil` or empty string"

More about configuration you can see **[here](/namespaces/script/#configuration)**