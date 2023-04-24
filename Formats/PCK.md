| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| PCK Type | (int32)0x4 | indicates PCK Format
| [Look-Up Table](./PCK.md#lookupTable) | variable | a list of all possible tags a file can have
| [File Entries](./PCK.md#entries) | variable | an index of all files within the PCK, contains size, type, and filename
| [File Contents](./PCK.md#contents) | variable | all files within the PCK, includes file tags

It is worth noting that aside from the main lineup(PS3, WiiU, and Xbox360) all other consoles are Endian Swapped.

## lookupTable

| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | (int32)0x4 | Amount of tags in the table

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Index | (int32)0x4 | numerical position within the table.
| Value | variable | a string(int16 indicates length, then Little endian Unicode string of specified length) indicating tag name

## entries


| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | (int32)0x4 | Amount of entries in the index

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| File Size | (int32)0x4 | indicates size in bytes of a file
| [File type](./PCK.md#File-Types) | (int32)0x4 | indicates type of file(Skin file, cape file, models, colours, etc)
| File Name | variable | a string(int16 indicates length, then Little endian Unicode string of specified length) indicating file name

## contents


| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| Count | (int32)0x4 | Amount of entries in the tag index
| Tags | variable | the tags and values of the file
| Data | variable | byte data of a file, size is the same as the applicable File Size value in Entries

(repeated per count)
| Name | Size (per element) | Description |
| :-:|:-:|:-:|
| tag key | (int32)0x4 | indicates key by index
| File Name | variable | a string(int16 indicates length, then Little endian Unicode string of specified length) indicating value of tag

## File Types


| ID | File Type | Extension |
| :-:|:-:|:-:|
| 0 |  Skin | *.png
| 1 |  Cape | *.png
| 2 |  Texture | *.png
| 3 |  UI Data | *.fui
| 4 |  Info | '0'
| 5 |  Texture Pack Info | (x16/x32/x64)Info.pck
| 6 |  Localisation | *.loc
| 7 |  Game Rules | GameRules.grf
| 8 |  Audio | audio.pck
| 9 |  Colour Table | colours.col
| 10 |  Game Rules Header | GameRules.grh
| 11 |  Skin Data | Skins.pck
| 12 |  Models | models.bin
| 13 |  Behaviours | behaviours.bin
| 14 |  Material | entityMaterials.bin




