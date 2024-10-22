> [!NOTE]
> COL is always Big Endian, regardless of console.

| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| COL Version | 0x04 (int32) | Indicates file version
| [Colours](./COL.md#Standard-Colours) | Variable | A list of all colours within the Colour Table
| [Water Colours](./COL.md#Water-Colours) | Variable (only exists if COL Version > 0) | A list of all water colours within the Colour Table

## Standard Colours

| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | 0x04 (int32) | Amount of Colours in the table

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Name | Variable (0x01 * length) | a UTF8 string (int16 indicates length) indicating Colour name
| Colour | 0x04 [(ARGB)](./COL.md#ARGB) | an ARGB value, indicating colour and transparency


## Water Colours

| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | 0x04 (int32) | Amount of Colours in the table

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Name | Variable (0x01 * length) | A UTF8 string (int16 indicates length) indicating Colour name
| Surface Colour | 0x04 [(ARGB)](./COL.md#ARGB) | an ARGB value, indicating colour and transparency
| Underwater Colour | 0x04 [(ARGB)](./COL.md#ARGB) | an ARGB value, indicating colour and transparency
| Fog Colour | 0x04 [(ARGB)](./COL.md#ARGB) | an ARGB value, indicating colour and transparency

## ARGB

| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Alpha | 0x01 (int8) | Alpha colour channel 
| Red | 0x01 (int8) | Red colour channel 
| Green | 0x01 (int8) | Green colour channel 
| Blue | 0x01 (int8) | Blue colour channel 
