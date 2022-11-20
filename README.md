# Nuron's Nightmare Executor Api
* [Structs](#structs)
* [Functions](#functions)
* [Class Methods](#classfunctions)
* [Hooks](#hooks)
* [Events](#events)

## ChangeLogs
- Vector4 removed :skull:
- Many things added.

## Structs
* [Vector2](#vector2)
* [Vector3](#vector3)
* [NightmareBot](#nightmarebot)
* [Inventory](#inventory)
* [InventoryItem](#inventoryitem)
* [World](#world)
* [Tile](#tile)
* [NetObject](#netobject)
* [NetAvatar](#netavatar)
* [Clothes](#clothes)
* [NPC](#npc)
* [GamePacket](#gamepacket)
* [ItemDatabase](#itemdatabase)
* [ItemInfo](#iteminfo)
* [HttpClient](#httpclient)
* [HttpResponse](#httpresponse)
* [RTVAR](#rtvar)

## Functions
* [sleep(ms) - Sleep(ms)](#sleep)
* [Json](#json)
* [GetBot](#getbot)
* [GetBots](#getbots)

## Class Methods
* [RTVAR::RTVAR](#rtvar_constructor)
* [RTVAR::GetParam](#getparam)
* [HttpClient::HttpClient](#httpclient_contructor)
* [HttpClient::GET](#GET)
* [HttpClient::POST](#POST)
* [HttpClient::setHeaders](#setHeaders)
* [Vector2::Vector2](#vector2_constructor)
* [Vector3::Vector3](#vector3_constructor)
* [ItemDatabase::GetItem](#db_GetItem)
* [ItemDatabase::GetItems](#db_GetItems)
* [Inventory::GetItem](#inv_GetItem)
* [Inventory::GetItems](#inv_GetItems)
* [World::GetTile](#gettile)
* [World::GetTiles](#gettiles)
* [World::GetPlayer](#getplayer)
* [World::GetPlayers](#getplayers)
* [World::GetObject](#getobject)
* [World::GetObjects](#getobjects)
* [World::GetNPC](#getnpc)
* [World::GetNPCs](#getnpcs)
* [NightmareBot::GetLocal](#getlocal)
* [NightmareBot::Hit](#hit)
* [NightmareBot::Wrench](#wrench)
* [NightmareBot::Place](#place)
* [NightmareBot::Enter](#enter)
* [NightmareBot::Wear](#wear)
* [NightmareBot::UnWear](#unwear)
* [NightmareBot::Drop](#drop)
* [NightmareBot::Trash](#trash)
* [NightmareBot::LeaveWorld](#leaveworld)
* [NightmareBot::Warp](#warp)
* [NightmareBot::Say](#say)
* [NightmareBot::FindPath](#findpath)
* [NightmareBot::FindWorldPath](#worldpath)
* [NightmareBot::SendRaw](#sendraw)
* [NightmareBot::SendGameMessage](#send3)
* [NightmareBot::SendGeneric](#send2)
* [NightmareBot::SendPacket](#sendstring)
* [NightmareBot::Connect](#connect)
* [NightmareBot::Disconnect](#disconnect)
* [NightmareBot::AddHook](#addhook)
* [NightmareBot::RemoveHook](#removehook)
* [NightmareBot::RemoveHooks](#removehooks)
* [NightmareBot::ToggleCollect](#togglecollect)


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

## NightmareBot
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `name` | Bot name |
| Bool | `connected` | is Connected |
| Inventory | `inventory` | Bot Inventory |
| World | `world` | Bot World |
| NetAvatar | `local` | Bot Local |

## InventoryItem
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `id` | Inventory Item's id |
| Number | `count` | Inventory Item's count |
| Bool | `isActive` | Inventory Item's active status |

## Inventory
| Type | Name | Description|
|:-----|:----:|:-----------|
| Table | `items` | Inventory Item Table |

## World
| Type | Name | Description|
|:-----|:----:|:-----------|
| string | `name` | World Name |
| Vector2 | `size` | World Size |
| Number | `tilecount` | World Tile Count |
| Number | `objectcount` | World Object Count |
| Table | `tiles` | Table Of World Tiles |
| Table | `objects` | Table Of World Objects |
| Table | `players` | Table Of World Players |
| Table | `npcs` | Table Of World NPCs |

## Tile
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `fg` | Tile Foreground ID |
| Number | `bg` | Tile Background ID |
| Number | `x` | Tile Position x |
| Number | `y` | Tile Position y |
| Number | `parent` | Tile parent |
| Number | `flags` | Tile Flags |
| TypeFlags | `typeflags` | Tile Type Flags |

## NetObject
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `id` | Item id |
| Number | `x` | Object Position x |
| Number | `y` | Object Position y |
| Number | `count` | Item count |
| Number | `flags` | Object flags |
| Number | `oid` | Object id |

## Clothes
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `hat` | Hat |
| Number | `shirt` | Shirt |
| Number | `pants` | Pants |
| Number | `shoes` | Shoes |
| Number | `face` | Face |
| Number | `hand` | Hand |
| Number | `wings` | Wings/Back |
| Number | `mask` | Mask |
| Number | `neck` | Neck |
| Number | `artifact` | Artifact |

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

## NPC
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `id` | NPC id/index |
| Number | `type` | NPC type |
| Vector2 | `position` | NPC's current position |
| Vector2 | `nextPosition` | Position that NPC is going to. |

## GamePacket
| Type | Name |
|:-----|:----:|
| Number | `type` |
| Number | `objtype` |
| Number | `count1` |
| Number | `count2` |
| Number | `netid` | 
| Number | `item` | 
| Number | `flags` | 
| Number | `float_var` |
| Number | `int_data` |
| Number | `vec_x` |
| Number | `vec_y` | 
| Number | `vec2_x` |
| Number | `vec2_y` |
| Number | `particle_rotation` |
| Number | `int_x` |
| Number | `int_y` | 

## ItemDatabase
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `itemCount` | Item Count |
| Number | `itemDatVersion` | item.dat Version |

## ItemInfo
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `name` | Item's Name |
| Number | `id` | Item's ID |
| Number | `editableType` | Item's Editable Type |
| Number | `itemCategory` | Item's Category |
| Number | `actionType` | Item's Action Type |
| Number | `hitSoundType` | Item's Hit Sound Type |
| Number | `itemKind` | Item's Kind |
| Number | `collisionType` | Item's Collision Type |
| Number | `dropChance` | Item's Drop Chance |
| Number | `clothingType` | Item's Clothing Type |
| Number | `rarity` | Item's Rarity |
| Number | `flags1` | Item's unk1 |
| Number | `flags2` | Item's unk2 |
| Number | `seedColor` | Item's Seed Color |
| Number | `seedOverlayColor` | Item's Seed Overlay Color |
| Number | `growTime` | Seed's Growtime |

## HttpClient
| Type | Name | Description|
|:-----|:----:|:-----------|

## HttpResponse
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `body` | Received Data |
| Number | `status` | HTTP Status |
| Number | `version` | HTTP Version |

## RTVAR
| Type | Name | Description|
|:-----|:----:|:-----------|
