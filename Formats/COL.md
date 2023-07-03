| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| COL Version | (int32)0x4 | indicates Format version
| [Colours](./COL.md#Standard-Colours) | variable | a list of all colours within the Colour Table
| [Water Colours](./COL.md#Water-Colours) | variable | a list of all water colours within the Colour Table(only if Version > 0)

## Standard Colours


| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | (int32)0x4 | Amount of Colours in the table

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Name | variable | a string(int16 indicates length, then Little endian Unicode string of specified length) indicating Colour name
| Colour | [(ARGB)](./COL.md#ARGB)0x4 | an ARGB value, indicating colour and transparency


## Water Colours


| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | (int32)0x4 | Amount of Colours in the table

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Name | variable | a string(int16 indicates length, then Little endian Unicode string of specified length) indicating Colour name
| Surface Colour | [(ARGB)](./COL.md#ARGB)0x4 | an ARGB value, indicating colour and transparency
| Underwater Colour | [(ARGB)](./COL.md#ARGB)0x4 | an ARGB value, indicating colour and transparency
| Fog Colour | [(ARGB)](./COL.md#ARGB)0x4 | an ARGB value, indicating colour and transparency

## ARGB

| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Alpha | (int8)0x1 | Alpha colour channel 
| Red | (int8)0x1 | Red colour channel 
| Green | (int8)0x1 | Green colour channel 
| Blue | (int8)0x1 | Blue colour channel 
