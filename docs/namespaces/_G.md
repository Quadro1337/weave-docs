# _G

### print
`print(output: any[, ...])`

|Name|Type|Description|
|:-|:-|:-|
|output|`any`|Output that will be printed to console|
|...|`any`|Optional arguments that will be printed separated by a space|

Prints the output to the console.

### pattern_scan
`pattern_scan(module: string, signature: string): number`

|Name|Type|Description|
|:-|:-|:-|
|module|`string`|Name of the module where the signature search will take place|
|signature|`string`|IDA style signature, the wildcard is "`?`"|

### create_interface
`create_interface(module: string, interface: string): number`

|Name|Type|Description|
|:-|:-|:-|
|module|`string`|Module name containing the interface|
|interface|`string`|Interface name|