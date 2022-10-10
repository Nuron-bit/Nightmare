# Nuron's Nightmare Executor Api
* [Structs](#structs)
* [Functions](#functions)
* [Hooks](#hooks)

## ChangeLogs
- Vector4 added

## Structs
* [Vector2](#vector2)
* [Vector3](#vector3)
* [Vector4](#vector4)
* [NetAvatar](#netavatar)
* [NetObject](#worldobject)
* [InventoryItem](#inventoryitem)
* [Inventory](#inventory)
* [Tile](#tile)
* [World](#world)
* [GamePacket](#gamepacket)
* [ItemInfo](#iteminfo)

## Vector2
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `x` | x axis |
| Number | `y` | y axis |


## Vector3
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `x` | x axis |
| Number | `y` | y axis |
| Number | `z` | z axis |


## Vector4
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `x` | x axis |
| Number | `y` | y axis |
| Number | `z` | z axis |
| Number | `d` | d axis |


## NetAvatar
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `name` | Player's name |
| String | `alt_name` | Player's alt name |
| Number | `netid` | Player's netid | 
| Number | `userid` | Player's userid | 
| Number | `x` | Player's position x | 
| Number | `y` | Player's position y | 
| Boolean | `isMod` | Player's mod status | 
| Boolean | `isSuperMod` | Player's smod status | 
| Boolean | `isLocal` | Player's local status | 
| Vector4 | `skincolor` | Player's skin color |
| Clothes | `clothes` | Player's clothes | 
