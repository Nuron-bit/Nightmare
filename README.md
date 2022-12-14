# Nuron's Nightmare Executor Api
* [Structs](#structs)
* [Functions](#functions)
* [Class Methods](#class-methods)
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
* [RTVAR:RTVAR](#rtvarrtvar)
* [RTVAR:GetParam](#rtvargetparam)
* [HttpClient:HttpClient](#httpclienthttpclient)
* [HttpClient:GET](#httpclientget)
* [HttpClient:POST](#httpclientpost)
* [HttpClient:setHeaders](#httpclientsetheaders)
* [Vector2:Vector2](#vector2vector2)
* [Vector3:Vector3](#vector3vector3)
* [ItemDatabase:GetItem](#itemdatabasegetitem)
* [ItemDatabase:GetItems](#itemdatabasegetitems)
* [Inventory:GetItem](#inventorygetitem)
* [Inventory:GetItems](#inventorygetitems)
* [World:GetTile](#worldgettile)
* [World:GetTiles](#worldgettiles)
* [World:GetPlayer](#worldgetplayer)
* [World:GetPlayers](#worldgetplayers)
* [World:GetObject](#worldgetobject)
* [World:GetObjects](#worldgetobjects)
* [World:GetNPC](#worldgetnpc)
* [World:GetNPCs](#worldgetnpcs)
* [NightmareBot:GetLocal](#nightmarebotgetlocal)
* [NightmareBot:Hit](#nightmarebothit)
* [NightmareBot:Wrench](#nightmarebotwrench)
* [NightmareBot:Place](#nightmarebotplace)
* [NightmareBot:Enter](#nightmarebotenter)
* [NightmareBot:Wear](#nightmarebotwear)
* [NightmareBot:UnWear](#nightmarebotunwear)
* [NightmareBot:Drop](#nightmarebotdrop)
* [NightmareBot:Trash](#nightmarebottrash)
* [NightmareBot:LeaveWorld](#nightmarebotleaveworld)
* [NightmareBot:Warp](#nightmarebotwarp)
* [NightmareBot:Say](#nightmarebotsay)
* [NightmareBot:FindPath](#nightmarebotfindpath)
* [NightmareBot:FindWorldPath](#nightmarebotfindworldpath)
* [NightmareBot:SendRaw](#nightmarebotsendraw)
* [NightmareBot:SendGameMessage](#nightmarebotsendgamemessage)
* [NightmareBot:SendGeneric](#nightmarebotsendgeneric)
* [NightmareBot:SendPacket](#nightmarebotsendpacket)
* [NightmareBot:Connect](#nightmarebotconnect)
* [NightmareBot:Disconnect](#nightmarebotdisconnect)
* [NightmareBot:AddHook](#nightmarebotaddhook)
* [NightmareBot:RemoveHook](#nightmarebotremovehook)
* [NightmareBot:RemoveHooks](#nightmarebotremovehooks)
* [NightmareBot:ToggleCollect](#nightmarebottogglecollect)

# Structures

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

# Functions

## sleep
`void sleep(int milliseconds)`

Sleeps thread

Example:
```lua
print("Hello")
sleep(1000)
print("World!)
```

## Json
`MultiTable Json(string json_text)`

Converts string to json table.

Example:
```lua
data = [[{
  "player_name": "Nuron",
  "player_age": 18
}]]

print(Json(data)["player_name"])
```

## GetBot
`NightmareBot* GetBot(string name)`

Gets bot via name

Example: 
```lua
bot = GetBot("Nuron")
bot:Say("i love Nightmare")
```

## GetBots
`Table<NightmareBot*> GetBots()`

Gets all bots. (returns NightmareBot Table)

Example: 
```lua
for i, bot in pairs(GetBots()) do
print(bot.name)
end
```

## Vector2:Vector2
`Vector2* Vector2(int x, int y)`

Vector2 Constructor.

Example: 
```lua
vc = Vector2(35, 46)
print(string.format("Vector2(x: %i, y: %i)", vc.x, vc.y))
```


## Vector3:Vector3
`Vector3* Vector3(int x, int y, int z)`

Vector3 Constructor.

Example: 
```lua
vc = Vector3(27, 43, 79)
print(string.format("Vector3(x: %i, y: %i, z: %i)", vc.x, vc.y, vc.z))
```


## RTVAR:RTVAR()
`RTVAR* RTVAR(string content)`

RTVAR Constructor.

Example: 
```lua
rtvar = RTVAR([[
name|Bongo
userid|69
]])
```


## RTVAR:GetParam
`string GetParam(string key)`

Gets Value by key/param.

Example: 
```lua
rtvar = RTVAR([[
name|Bongo
userid|69
]])

print(rtvar:GetParam("name"))
-- (Seems useless for you? You can parse many packets like OnSpawn)
```


## HttpClient:HttpClient
`HttpClient* HttpClient(string url)`

HttpClient Constructor

Example: 
```lua
client = HttpClient("https://www.growtopiagame.com")
```


## HttpClient:GET
`HttpResponse* GET(string path)`

HTTP GET Request

Example: 
```lua
client = HttpClient("https://www.growtopiagame.com")
response = client:GET('/')

print(response.body)
```


## HttpClient:POST
`HttpResponse* POST(string path, string content, string content_type)`

HTTP POST Request

Example: 
```lua
client = HttpClient("https://catalog.roblox.com")
response = client:POST("path_here", "content_here", "content_type_here")
```


## HttpClient:setHeaders
`void setHeaders(Table<string, string> headers)`

Used for setting custom headers.

Example: 
```lua
client = HttpClient("https://www.growtopiagame.com")
headers = {}
headers["User-Agent"] = "Nightmare+"

client:setHeaders(headers)
```


## ItemDatabase:GetItem
`static ItemInfo* GetItem(int id)`

Returns item info via item id.

Example: 
```lua
-- In Nightmare, there is static ItemDatabase class defined.
item = ItemDatabase.GetItem(2)

print(string.format("{ item_name: %s, item_actionType: %i }",
  item.name,
  item.actionType))
```


## ItemDatabase:GetItems
`static Table<ItemInfo*> GetItems()`

Returns items table.

Example: 
```lua
for i, item_info in pairs(ItemDatabase.GetItems()) do
print(string.format("name: %s, id: %i", item_info.name, item_info.id))
end
```


## Inventory:GetItem
`InventoryItem* GetItem(int id)`

Returns inventory item by id.

Example: 
```lua
bot = GetBot("Nightmare")
inventory = bot:GetInventory()
print(inventory:GetItem(242).count)
```


## Inventory:GetItems
`Table<InventoryItem*> GetItem()`

Returns inventory items as table.

Example: 
```lua
for i, item in pairs(GetBot("Nightmare"):GetInventory():GetItems()) do
print(string.format("{ item_id: %i; item_count: %i; }", item.id, item.count))
end
```


## World:GetTile
`Tile* GetTile(int tileX, int tileY)`

Returns tile by world tile position.

Example: 
```lua
for i, bot in pairs(GetBots()) do
if(bot:GetWorld():GetTile(0,0).id == 242) then print("World lock found!") end
end
```


## World:GetTiles
`Table<Tile*> GetTiles()`

Returns world Tiles.

Example: 
```lua
dirt_count = 0
for i, tile in pairs(GetBot("Nightmare"):GetWorld():GetTiles()) do 
  if tile.id == 2 then dirt_count = dirt_count + 1 end
end

print("Found "..dirt_count.." dirt!")
```


## World:GetPlayer
`NetAvatar* GetPlayer(string growid)`

Returns player.

Example: 
```lua
player = GetBot("Nightmare"):GetWorld():GetPlayer("Nuron")
print(player.name)
```


## World:GetPlayers
`Table<NetAvatar*> GetPlayers()`

Returns player list.

Example: 
```lua
bot = GetBot("Nightmare")
for i, player in pairs(bot:GetWorld():GetPlayers()) do
bot:Say(string.format("/ban %s", player.name))
end
```


## World:GetObject
`NetObject* GetObject(int object_id)`

Returns object.

Example: 
```lua
bot = GetBot("Nightmare")
bot:Collect(bot:GetWorld():GetObject(1))
```


## World:GetObjects
`Table<NetObject*> GetObjects()`

Returns object list.

Example: 
```lua
bot = GetBot("Nightmare")
for i, obj in pairs(bot:GetWorld():GetObjects()) do
print(string.format("Found %s in position (%i, %i).", ItemDatabase.GetItem(obj.id).name, obj.x, obj.y))
end
```


## World:GetNPC
`NPC* GetNPC(int npc_index)`

Returns NPC.

Example: 
```lua
npc = GetBot("Nightmare"):GetWorld():GetNPC(0)
if npc then
print("World has npc!")
end
```


## World:GetNPCs
`Table<NPC*> GetNPCs()`

Returns NPC list.

Example: 
```lua
npc = GetBot("Nightmare"):GetWorld():GetNPC(0)
if npc then
print("World has npc!")
end
```


## NightmareBot:GetLocal
`NetAvatar* GetLocal()`

Returns local net avatar.

Example: 
```lua
localbot = GetBot("Nightmare"):GetLocal()
if localbot then
print(string.format("Bot is in position (%i, %i)", localbot.x, localbot.y))
end
```


## NightmareBot:FindPath
`bool FindPath(int x, int y)`

PathFinder.

Example: 
```lua
GetBot("Nightmare"):FindPath(36, 36)
```


## NightmareBot:FindWorldPath
`bool FindWorldPath(float x, float y)`

PathFinder.

Example: 
```lua
GetBot("Nightmare"):FindWorldPath(420, 69)
```


## NightmareBot:Hit
`bool Hit(int tileX, int tileY)`

For hitting Tile.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Hit(36, 36) end
end
```


## NightmareBot:Wrench
`bool Wrench(int tileX, int tileY)`

For wrenching Tile.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Wrench(36, 36) end
end
```


## NightmareBot:Place
`bool Place(int tileX, int tileY, int itemID)`

For placing blocks.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Place(36, 36, 242) end
end
```


## NightmareBot:Enter
`bool Enter()`

For entering door in bot position.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Enter() end
end
```


## NightmareBot:Wear
`bool Wear(int itemID)`

For wearing clothes.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Wear(1784) end
end
```


## NightmareBot:UnWear
`bool UnWear(int itemID)`

For unwearing clothes.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:UnWear(1784) end
end
```


## NightmareBot:Drop
`bool Drop(int itemID, int itemCount)`

For dropping inventory items.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Drop(7188, 1) end
end
```


## NightmareBot:Trash
`bool Trash(int itemID, int itemCount)`

For trashing inventory items.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Trash(2, 200) end
end
```


## NightmareBot:LeaveWorld
`void LeaveWorld()`

For leaving world.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected and bot:GetWorld() then
  bot:LeaveWorld()
end
```


## NightmareBot:Warp
`void Warp(string worldName, string doorID)`

For warping.

Example: 
```lua
bot = GetBot("Nightmare")

bot:Warp("JACKBOWE")
```


## NightmareBot:Say
`void Say(string Text)`

For chatting.

Example: 
```lua
bot = GetBot("Nightmare")
bot:Say("Im noob :(")
```


## NightmareBot:SendRaw
`void SendRaw(GamePacket packet)`

For sending raw packet.

Example: 
```lua
bot = GetBot("Nightmare")

packet = {}
packet.type = 0
packet.int_x = -1
packet.int_y = -1
packet.vec_x = bot:GetLocal().x - 32
packet.vec_y = bot:GetLocal().y

bot:SendRaw(packet)

-- Moves bot to left.
```


## NightmareBot:SendGameMessage
`void SendGameMessage(string packet)`

For sending game message.

Example: 
```lua
bot = GetBot("Nightmare")
bot:SendGameMessage("action|join_request\nname|Github\ninvitedWorld|0")
```


## NightmareBot:SendGeneric
`void SendGeneric(string packet)`

For sending generic text.

Example: 
```lua
bot = GetBot("Nightmare")
bot:SendGeneric("generic_text")
```


## NightmareBot:SendPacket
`void SendPacket(int type, string packet)`

For sending packets via types.

Example: 
```lua
bot = GetBot("Nightmare")
bot:SendPacket(2, "action|dialog_return\ndialog_name|Executor")
```


## NightmareBot:Connect
`bool Connect()`

For connecting to gt server.

Example: 
```lua
bot = GetBot("Nightmare")

if not bot.connected then
  bot:Connect()
end
```


## NightmareBot:Disconnect
`void Disconnect()`

For disconnecting from gt server.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  bot:Disconnect()
end
```


## NightmareBot:AddHook
`void AddHook(enum<HookTypes> HookType, luaFunction function)`

For adding hooks/callbacks.

Example: 
```lua
bot = GetBot("Nightmare")

function onReceivedVariantList(var)
print(var[0])
end

bot:AddHook(OnVariantList, onReceivedVariantList)
```


## NightmareBot:RemoveHook
`void RemoveHook(enum<HookTypes> HookType)`

For removing specific hook.

Example: 
```lua
bot = GetBot("Nightmare")
bot:RemoveHook(OnVariantList)
```


## NightmareBot:RemoveHooks
`void RemoveHooks()`

For removing all hooks.

Example: 
```lua
bot = GetBot("Nightmare")
bot:RemoveHooks()
```


## NightmareBot:ToggleCollect
`void ToggleCollect(bool isActive)`

For toggling autocollect mode.

Example: 
```lua
bot = GetBot("Nightmare")
bot:ToggleCollect(true)
```

# Hooks

## OnVariantList

Example:
```lua
bot = GetBot("Nightmare")

function onVar(bot, var)
if var[0] == "OnSpawn" and bot.name == "Nightmare" then
  rtvar = RTVAR(var[1])
  print(string.format("Player %s entered the world!", 
  rtvar:GetParam("name"))
end
end

bot:AddHook(OnVariantList, onVar)
```
## OnGameMessage
## OnGenericText
## OnTrackPacket
## OnGamePacket
