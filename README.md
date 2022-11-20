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
* [NightmareBot](#bot)
* [Inventory](#inventory)
* [InventoryItem](#inventoryitem)
* [World](#world)
* [Tile](#tile)
* [NetObject](#worldobject)
* [NetAvatar](#netavatar)
* [NPC](#npc)
* [GamePacket](#gamepacket)
* [ItemDatabase](#ItemDatabase)
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
