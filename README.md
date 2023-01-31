# Nuron's Nightmare Executor Api
* [Structs](#structs)
* [Functions](#functions)
* [Class Methods](#class-methods)
* [Hooks](#hooks)
* [Events](#events)

## ChangeLogs
- Updated Classes and added Hooks.

## Enums
* [Packet Type](#packettype)
* [Bubble Type](#bubbletype)
* [Captcha Status](#captchastatus)
* [Bot Status](#botstatus)
* [Http Status](#httpstatus)

## Structs
* [Vector2](#vector2)
* [Vector3](#vector3)
* [Embed](#embed)
* [Webhook](#webhook)
* [Bot](#bot)
* [Inventory](#inventory)
* [InventoryItem](#inventoryitem)
* [World](#world)
* [Tile](#tile)
* [NetObject](#netobject)
* [NetAvatar](#netavatar)
* [Clothes](#clothes)
* [NPC](#npc)
* [GamePacket](#gamepacket)
* [ItemInfo](#iteminfo)
* [HttpClient](#httpclient)
* [HttpResult](#httpresult)
* [RTVAR](#rtvar)

## Functions
* [sleep(ms) - Sleep(ms)](#sleep)
* [GetBot](#getbot)
* [GetBots](#getbots)
* [GetItemInfo](#getiteminfo)
* [GetItemInfos](#getiteminfos)
* [RemoveColor](#removecolor)

## Class Methods
### RTVAR
* [RTVAR(string text)](#rtvarrtvar)
* [GetParam](#rtvargetparam)
* [GetIntParam](#rtvargetintparam)
* [GetLongParam](#rtvargetlongparam)
* [FindKey](#rtvarfindkey)

### HttpClient
* [HttpClient()](#httpclienthttpclient)
* [SetURL](#httpclientseturl)
* [SetPath](#httpclientsetpath)
* [AddHeader](#httpclientaddheader)
* [RemoveHeader](#httpclientremoveheader)
* [SetContentType](#httpclientsetcontenttype)
* [GET](#httpclientget)
* [POST](#httpclientpost)

### HttpResult
* [GetError](#httpresultgeterror)

### Webhook
* [SendWebhook](#webhooksendwebhook)

### Bot
* [Connect](#botconnect)
* [Disconnect](#botdisconnect)
* [GetInventory](#botgetinventory)
* [GetWorld](#botgetworld)
* [GetLocal](#botgetlocal)
* [Drop](#botdrop)
* [Trash](#bottrash)
* [Enter](#botenter)
* [Hit](#bothit)
* [Place](#botplace)
* [Say](#botsay)
* [Wear](#botwear)
* [Unwear](#botunwear)
* [Warp](#botwarp)
* [Wrench](#botwrench)
* [WrenchPlayer](#botwrenchplayer)
* [MoveDown](#botmovedown)
* [MoveUp](#botmoveup)
* [MoveRight](#botmoveright)
* [MoveLeft](#botmoveleft)
* [FindPath](#botfindpath)
* [FindWorldPath](#botfindworldpath)
* [LeaveWorld](#botleaveworld)
* [SendGameMessage](#botsendgamemessage)
* [SendGeneric](#botsendgeneric)
* [SendRaw](#botsendraw)
* [SendPacket](#botsendpacket)
* [SetBubbleState](#botsetbubblestate)
* [ToggleCollect](#bottogglecollect)
* [AddHook](#botaddhook)
* [RemoveHook](#botremovehook)
* [RemoveHooks](#botremovehooks)

### Inventory
* [GetItem](#inventorygetitem)
* [GetItems](#inventorygetitems)
* [FindItem](#inventoryfinditem)
* [GetItemCount](#inventorygetitemcount)
* [isItemActive](#inventoryisitemactive)
* [isEmpty](#inventoryisempty)

### World
* [GetTile](#worldgettile)
* [GetTiles](#worldgettiles)
* [GetObject](#worldgetobject)
* [GetObjects](#worldgetobjects)
* [GetPlayer](#worldgetplayer)
* [GetPlayers](#worldgetplayers)
* [GetNPC](#worldgetnpc)
* [GetNPCs](#worldgetnpcs)
* [GetAccessList](#worldgetaccesslist)

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

## Bot
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `name` | Bot name |
| BotStatus | `status` | Bot status |
| Bool | `connected` | is Connected |
| Bool | `connecting` | is Connecting |
| Bool | `reconnecting` | is Reconnecting |
| Inventory | `inventory`| Bot Inventory |
| World | `world` | Bot World |
| NetAvatar | `local` | Bot Local |
| Number | `netid` | Bot netid |
| Number | `userid` | Bot userid |
| String | `token` | Bot token |
| String | `uuidToken` | Bot UUID Token |
| Number | `gems` | Gem count |
| Number | `pearls` | Pearl count |
| Bool | `autoAccess` | is AutoAccess Enabled |
| Bool | `autoBan` | is AutoBan Enabled |
| Bool | `autoLeave` | is AutoLeave Enabled |
| Bool | `autoTutorial` | is AutoTutorial Enabled |
| CaptchaStatus | `captchaStatus` | Captcha Status |
| Number | `collectInterval` | Collect Interval as miliseconds |
| Number | `collectRange` | Collect Range |
| Bool | `autocollect` | is AutoCollect Enabled |
| Bool | `ignoreEssence` | is IgnoreEssence Enabled |
| Bool | `ignoreGem` | is IgnoreGem Enabled |
| Bool | `inGame` | is Bot inGame |
| Bool | `isAccountSecured` | is Account Secured |
| Bool | `isMoving` | is Bot Moving |
| Bool | `hasCaptcha` | is Solving Captcha |
| Bool | `solvedCaptcha` | is Solved Captcha |

## InventoryItem
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `id` | Inventory Item's id |
| Number | `count` | Inventory Item's count |
| Bool | `isActive` or `active` | Inventory Item's active status |

## Inventory
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `version` | Inventory Version |
| Number | `slotCount` | Inventory Slot Count |
| Number | `itemCount` | Inventory Item Count |
| Table | `items` | Inventory Items, accessed by GetItems() |

## World
| Type | Name | Description|
|:-----|:----:|:-----------|
| string | `name` | World Name |
| Number | `width` | World width |
| Number | `height` | World height |
| Number | `lockX` | World Lock Tile X |
| Number | `lockY` | World Lock Tile Y |
| Number | `tileCount` | World Tile Count |
| Table | `tiles` | Table Of World Tiles, accessed by GetTiles() |
| Table | `objects` | Table Of World Objects, accessed by GetObjects() |
| Table | `players` | Table Of World Players, accessed by GetPlayers() |
| Table | `npcs` | Table Of World NPCs, accessed by GetNPCs() |

## Tile
| Type | Name | Description|
|:-----|:----:|:-----------|
| Number | `fg` or `foreground` | Tile Foreground ID |
| Number | `bg` or `background` | Tile Background ID |
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
| Number | `pants` or `pant` | Pants |
| Number | `shoes` or `shoe` | Shoes |
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
| Number | `userid` or `uid` | Player's userid | 
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
| Number | `x` | NPC Position X |
| Number | `y` | NPC Position Y |
| Number | `dest_x` | NPC Destination X |
| Number | `dest_y` | NPC Destination Y |

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
| Number | `clothingType` | Item's Clothing Type |
| Number | `rarity` | Item's Rarity |
| Number | `flags1` | Item's unk1 |
| Number | `flags2` | Item's unk2 |
| Number | `seedColor` | Item's Seed Color |
| Number | `seedOverlayColor` | Item's Seed Overlay Color |
| Number | `growTime` | Seed's Growtime |

## Embed
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `title` | Embed Title |
| String | `description` | Embed Description |
| String | `url` | Embed Url |
| Number | `color` | Embed Color |

## Webhook
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `username` | Webhook Username |
| String | `content` | Webhook content |
| String | `embed` | Webhook Embed (only one) |
| String | `allow_mentions` | Webhook Mentions |
| String | `avatar` | Webhook Avatar URL |
| String | `url` | Webhook URL |

## HttpClient
| Type | Name | Description|
|:-----|:----:|:-----------|

## HttpResult
| Type | Name | Description|
|:-----|:----:|:-----------|
| String | `body` | Received Data |
| HttpStatus | `status` | HTTP Status |

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
`Bot* GetBot(string name)`

Gets bot via name

Example: 
```lua
bot = GetBot("Nuron")
bot:Say("i love Nightmare")
```

## GetBots
`Table<Bot*> GetBots()`

Gets all bots. (returns NightmareBot Table)

Example: 
```lua
for i, bot in pairs(GetBots()) do
print(bot.name)
end
```

## GetItemInfo
`static ItemInfo* GetItemInfo(int id)`

Returns item info via item id.

Example: 
```lua
item = GetItemInfo(2)

print(string.format("{ item_name: %s, item_actionType: %i }",
  item.name,
  item.actionType))
```


## GetItemInfos
`static Table<ItemInfo*> GetItemInfos()`

Returns item infos table.

Example: 
```lua
for i, item_info in pairs(GetItemInfos()) do
print(string.format("name: %s, id: %i", item_info.name, item_info.id))
end
```

## RemoveColor
`string RemoveColor()`

Clears colors from a text.

Example: 
```lua
colorful_text = "`1Hello `2user`0!"
normal_text = RemoveColor(colorful_text) -- Which equals to "Hello user!"
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

## RTVAR:GetIntParam
`number GetIntParam(string key)`

Gets int Value by key.

Example: 
```lua
rtvar = RTVAR([[
name|Bongo
userid|69
]])

print(rtvar:GetIntParam("userid"))
```

## RTVAR:GetLongParam
`number GetLongParam(string key)`

Gets long int Value by key.

Example: 
```lua
rtvar = RTVAR([[
name|Bongo
userid|69999999999
]])

print(rtvar:GetLongParam("userid"))
```

## RTVAR:FindKey
`bool FindKey(string key)`

Check if key exists.

Example: 
```lua
rtvar = RTVAR([[
name|Bongo
userid|69999999999
]])

if rtvar:FindKey("name") then
  print("Found key name!")
end
```

## HttpClient:HttpClient
`HttpClient* HttpClient()`

HttpClient Constructor

Example: 
```lua
client = HttpClient()
```

## HttpClient:SetURL
`void SetURL(string url)`

Sets url.

Example: 
```lua
client = HttpClient()
client:SetURL("https://www.google.com")
```

## HttpClient:SetPath
`void SetPath(string path)`

Sets path.

Example: 
```lua
client = HttpClient()
client:SetURL("https://www.google.com")
client:SetPath("/some/random/path/")
```

## HttpClient:AddHeader
`void AddHeader(string key, string value)`

Adds custom header.

Example: 
```lua
client = HttpClient()
client:SetURL("https://www.google.com")
client:SetPath("/some/random/path/")

client:AddHeader("User-Agent", "Nightmare-Bot-Api")
```

## HttpClient:RemoveHeader
`void RemoveHeader(string key)`

Removes custom header if exists.

Example: 
```lua
client = HttpClient()
client:SetURL("https://www.google.com")
client:SetPath("/some/random/path/")

client:AddHeader("User-Agent", "Nightmare-Bot-Api")
client:RemoveHeader("User-Agent")
```

## HttpClient:SetContentType
`void SetContentType(string type)`

Sets content type of data.

Example: 
```lua
client = HttpClient()
client:SetURL("https://www.google.com")
client:SetPath("/some/random/path/")

client:AddHeader("User-Agent", "Nightmare-Bot-Api")

client:SetContentType("application/json")
```

## HttpClient:GET
`HttpResult* GET(string path = "")`

HTTP GET Request

Example: 
```lua
client = HttpClient()
client:SetURL("https://www.google.com")

response1 = client:GET()
response2 = client:GET("/some/custom/path/")

print(response1.body)
```

## HttpClient:POST
`HttpResult* POST(string path, string content)`

HTTP POST Request

Example: 
```lua
client = HttpClient()
client:SetURL("https://catalog.roblox.com")
client.SetContentType("application/json")
response = client:POST("", "{ }")
```

## HttpResult:GetError
`number GetError()`

returns HTTP error value.

Example: 
```lua
client = HttpClient()
client:SetURL("https://catalog.roblox.com")
response = client:GET()

print("Error Value: "..response:GetError())
```

## Webhook:SendWebhook
`void SendWebhook()`

Sends webhook.

Example: 
```lua
wh = Webhook("your_webhook_url")
wh.username = "Nightmare Bot"
wh.embed.title = "Test"
wh.embed.description = "This is a test webhook!"

wh:SendWebhook()
```

## Inventory:GetItem
`InventoryItem* GetItem(int id)`

Returns inventory item by id.

Example: 
```lua
bot = GetBot("Nightmare")
inventory = bot:GetInventory()
print(GetItemInfo(242).count)
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

## Inventory:GetItemCount
`Number GetItemCount(Number id)`

Returns item count by id. 

Example: 
```lua
count = GetBot("Wild"):GetInventory():GetItemCount(1784)

if count == 0 then
  print(string.format("Poor wild doesn't have %s", GetItemInfo(1784).name))
end
```

## Inventory:FindItem
`Number FindItem(Number id)`

Returns item count by id. 

Example: 
```lua
count = GetBot("Wild"):GetInventory():FindItem(1784)

if count == 0 then
  print(string.format("Poor wild doesn't have %s", GetItemInfo(1784).name))
end
```

## Inventory:isItemActive
`Bool isItemActive(Number id)`

Returns true if bot is currently wearing the item. 

Example: 
```lua
is_wearing = GetBot("Wild"):GetInventory():isItemActive(1784)

if is_wearing then
  print("Bot is currently wearing an item.")
end
```

## Inventory:isEmpty
`Bool isEmpty()`

Returns true if bot inventory is empty which means never. (Because of fist and wrench)

Example: 
```lua
is_inventory_empty = GetBot("Wild"):GetInventory():isEmpty()

if is_inventory_empty then
  print("Where is the fist and wrench?")
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
print(string.format("Found %s in position (%i, %i).", GetItemInfo(obj.id).name, obj.x, obj.y))
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
npc_list = GetBot("Nightmare"):GetWorld():GetNPCs()
for _, npc in pairs(npc_list) do
print("Npc id: "..npc.id)
end
```

## World:GetAccessList
`Table<Number> GetAccessList()`

Returns admin userids.

Example: 
```lua
for _, admin in pairs(GetBot("Wild"):GetWorld():GetAccessList()) do
  print("Admin found, userid: ", admin)
end
```

## Bot:GetWorld
`World* GetWorld()`

Returns bot world.

Example: 
```lua
world = GetBot("Nightmare"):GetWorld()
print(world.name)
```

## Bot:GetInventory
`Inventory* GetInventory()`

Returns bot inventory.

Example: 
```lua
bot = GetBot("Nightmare")
inventory = bot:GetInventory()

for _, item in pairs(inventory:GetItems()) do
  bot:Drop(item.id, item.count)
end
```

## Bot:GetLocal
`NetAvatar* GetLocal()`

Returns local net avatar.

Example: 
```lua
localbot = GetBot("Nightmare"):GetLocal()
if localbot then
print(string.format("Bot is in position (%i, %i)", localbot.x, localbot.y))
end
```


## Bot:FindPath
`bool FindPath(int x, int y)`

PathFinder.

Example: 
```lua
GetBot("Nightmare"):FindPath(36, 36)
```


## Bot:FindWorldPath
`bool FindWorldPath(float x, float y)`

PathFinder.

Example: 
```lua
GetBot("Nightmare"):FindWorldPath(420, 69)
```


## Bot:Hit
`bool Hit(int tileX, int tileY)`

For hitting Tile.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Hit(36, 36) end
end
```


## Bot:Wrench
`bool Wrench(int tileX, int tileY)`

For wrenching Tile.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Wrench(36, 36) end
end
```

## Bot:WrenchPlayer
`void WrenchPlayer(Number netid)`

To wrench a player by netid.

Example: 
```lua
GetBot("Sogga"):WrenchPlayer(1)
```

## Bot:Place
`bool Place(int tileX, int tileY, int itemID)`

For placing blocks.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Place(36, 36, 242) end
end
```


## Bot:Enter
`bool Enter()`

For entering door in bot position.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Enter() end
end
```


## Bot:Wear
`bool Wear(int itemID)`

For wearing clothes.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Wear(1784) end
end
```


## Bot:Unwear
`bool Unwear(int itemID)`

For unwearing clothes.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Unwear(1784) end
end
```


## Bot:Drop
`bool Drop(int itemID, int itemCount)`

For dropping inventory items.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Drop(7188, 1) end
end
```


## Bot:Trash
`bool Trash(int itemID, int itemCount)`

For trashing inventory items.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  if bot:GetLocal() then bot:Trash(2, 200) end
end
```


## Bot:LeaveWorld
`void LeaveWorld()`

For leaving world.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected and bot:GetWorld() then
  bot:LeaveWorld()
end
```


## Bot:Warp
`void Warp(string worldName, string doorID)`

For warping.

Example: 
```lua
bot = GetBot("Nightmare")

bot:Warp("JACKBOWE")
```


## Bot:Say
`void Say(string Text)`

For chatting.

Example: 
```lua
bot = GetBot("Nightmare")
bot:Say("Im noob :(")
```

## Bot:MoveRight
`void MoveRight()`

Bot Moves to Right.

Example: 
```lua
GetBot("Nigmare"):MoveRight()
```

## Bot:MoveLeft
`void MoveLeft()`

Bot Moves to Left.

Example: 
```lua
GetBot("Nigmare"):MoveLeft()
```

## Bot:MoveUp
`void MoveUp()`

Bot Moves to Up.

Example: 
```lua
GetBot("Nigmare"):MoveUp()
```

## Bot:MoveDown
`void MoveDown()`

Bot Moves to Down.

Example: 
```lua
GetBot("Nigmare"):MoveDown()
```

## Bot:SetBubbleState
`void SetBubbleState(BubbleType type)`

Sets bubble state of bot.

Example: 
```lua
GetBot("Sogga"):SetBubbleState(BUBBLE_WRENCH)
```

## Bot:SendRaw
`void SendRaw(GamePacket packet)`

For sending raw packet.

Example: 
```lua
bot = GetBot("Nightmare")

packet = GameUpdatePacket()
packet.type = 0
packet.int_x = -1
packet.int_y = -1
packet.vec_x = bot:GetLocal().x - 32
packet.vec_y = bot:GetLocal().y

bot:SendRaw(packet)

-- Moves bot to left.
```


## Bot:SendGameMessage
`void SendGameMessage(string packet)`

For sending game message.

Example: 
```lua
bot = GetBot("Nightmare")
bot:SendGameMessage("action|join_request\nname|Github\ninvitedWorld|0")
```


## Bot:SendGeneric
`void SendGeneric(string packet)`

For sending generic text.

Example: 
```lua
bot = GetBot("Nightmare")
bot:SendGeneric("generic_text")
```


## Bot:SendPacket
`void SendPacket(int type, string packet)`

For sending packets via types.

Example: 
```lua
bot = GetBot("Nightmare")
bot:SendPacket(2, "action|dialog_return\ndialog_name|Executor")
```

## Bot:Connect
`bool Connect()`

For connecting to gt server.

Example: 
```lua
bot = GetBot("Nightmare")

if not bot.connected then
  bot:Connect()
end
```

## Bot:Disconnect
`void Disconnect()`

For disconnecting from gt server.

Example: 
```lua
bot = GetBot("Nightmare")

if bot.connected then
  bot:Disconnect()
end
```

## Bot:AddHook
`void AddHook(enum<HookTypes> HookType, luaFunction function)`

For adding hooks/callbacks.

Example: 
```lua
bot = GetBot("Nightmare")

function onReceivedVariantList(bot, var)
print(var[0])
end

bot:AddHook(OnVariantList, onReceivedVariantList)
```


## Bot:RemoveHook
`void RemoveHook(enum<HookTypes> HookType)`

For removing specific hook by type.

Example: 
```lua
bot = GetBot("Nightmare")
bot:RemoveHook(OnVariantList)
```


## Bot:RemoveHooks
`void RemoveHooks()`

For removing all hooks.

Example: 
```lua
bot = GetBot("Nightmare")
bot:RemoveHooks()
```


## Bot:ToggleCollect
`void ToggleCollect(bool isActive)`

For toggling autocollect mode.

Example: 
```lua
bot = GetBot("Nightmare")
bot:ToggleCollect(true)
```

# Hooks

## OnVariantList

**Function Definition:**
```lua
function(NightmareBot* bot, Table<Variant> variantList)
```

**Example:**
```lua
bot = GetBot("Nightmare")

function onVar(bot, var)
if var[0] == "OnSpawn" and bot.name == "Nightmare" then
  rtvar = RTVAR(var[1])
  if rtvar:FindKey("name") then
    print(string.format("Player %s entered the world!", 
    rtvar:GetParam("name"))
  end
end
end

bot:AddHook(OnVariantList, onVar)
```

## OnGameMessage

**Function Definition:**
```lua
function(NightmareBot* bot, string game_message)
```

**Example:**
```lua
bot = GetBot("Nightmare")

function onMessage(bot, message)
print(message)
end

bot:AddHook(OnGameMessage, onMessage)
```

## OnGenericText

**Function Definition:**
```lua
function(NightmareBot* bot, string generic_text)
```

**Example:**
```lua
bot = GetBot("Nightmare")

function onGeneric(bot, message)
print(message)
end

bot:AddHook(OnGenericText, onGeneric)
```

## OnTrackPacket

**Function Definition:**
```lua
function(NightmareBot* bot, string packet)
```

**Example:**
```lua
bot = GetBot("Nightmare")

function onTrack(bot, packet)
print("Track Ev: "..RTVAR(packet):GetParam("eventName"))
end

bot:AddHook(OnTrackPacket, onTrack)
```

## OnGamePacket

**Function Definition:**
```lua
function(NightmareBot* bot, GameUpdatePacket* packet)
```

**Example:**
```lua
bot = GetBot("Nightmare")

function onPacket(bot, packet)
print(string.format("Raw Type: %d", packet.type))
if packet.type == 4 then
 print("Bot entered a world!")
end
end

bot:AddHook(OnGamePacket, onPacket)
```

