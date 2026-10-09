-- Tony's Hub - Complete GUI with Key System
-- Key to open: tony
-- All text in English

local WindUI = loadstring(game:HttpGet("https://github.com/Footagesus/WindUI/releases/latest/download/main.lua"))()

-- ==========================================
-- KEY SYSTEM
-- ==========================================
local CORRECT_KEY = "tony"

local KeyWindow = WindUI:CreateWindow({
    Title = "Tony's Hub - Key System",
    Icon = "rbxassetid://10734898355",
    Author = "Tony",
    Folder = "TonysHubKey",
    Size = UDim2.fromOffset(400, 260),
    Transparent = true,
    Theme = "Dark",
    User = { Enabled = true, Anonymous = true },
    SideBarWidth = 0,
    HasOutline = false,
})

local KeyTab = KeyWindow:Tab({
    Title = "Enter Key",
    Icon = "rbxassetid://10734898355",
})

local enteredKey = ""

KeyTab:Input({
    Title = "Key",
    Description = "Enter the key to access Tony's Hub",
    Placeholder = "Enter key here...",
    Value = "",
    Callback = function(text)
        enteredKey = text
    end,
})

KeyTab:Button({
    Title = "Verify Key",
    Description = "Click to verify your key",
    Callback = function()
        if enteredKey == CORRECT_KEY then
            WindUI:Notify({ Title = "Success", Content = "Key correct! Loading Tony's Hub...", Duration = 3 })
            KeyWindow:Destroy()
            task.wait(0.5)
            loadTonyHub()
        else
            WindUI:Notify({ Title = "Error", Content = "Invalid key! Try again.", Duration = 3 })
        end
    end,
})

-- ==========================================
-- MAIN HUB (only loads after correct key)
-- ==========================================
function loadTonyHub()

    local Window = WindUI:CreateWindow({
        Title = "Tony's Hub",
        Icon = "rbxassetid://10734898355",
        Author = "Tony",
        Folder = "TonysHub",
        Size = UDim2.fromOffset(620, 500),
        Transparent = true,
        Theme = "Dark",
        User = { Enabled = true, Anonymous = true },
        SideBarWidth = 200,
        HasOutline = false,
    })

    -- ==========================================
    -- TAB: BLOX FRUITS
    -- ==========================================
    local BloxFruitsTab = Window:Tab({ Title = "Blox Fruits", Icon = "rbxassetid://10734898355" })

    BloxFruitsTab:Button({
        Title = "GHOSTYHUB [NO KEY]",
        Description = "Auto Attack, Fruit Teleport, Bypass Speed",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ShowScript79/cokkahub/refs/heads/main/cokkahub"))()
        end,
    })

    BloxFruitsTab:Button({
        Title = "Cokka Hub [NO KEY]",
        Description = "Auto Farm Level, Boss, Materials, Dungeons",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ShowScript79/cokkahub/refs/heads/main/cokkahub"))()
        end,
    })

    BloxFruitsTab:Button({
        Title = "Gravity Hub [NO KEY]",
        Description = "Auto Farm, Fishing, Magnet, Raids",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Dev-GravityHub/BloxFruit/main/MainPremium.lua"))()
        end,
    })

    BloxFruitsTab:Button({
        Title = "Arxki Hub [KEY]",
        Description = "PvP: Aimlock, Silent Aim, Fruit Magnet (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://api.jnkie.com/api/v1/luascripts/public/aacde3676be5688ad17cbf78842b8e6061834b0cd70a82298f3b1600d8d2c690/download"))()
        end,
    })

    -- ==========================================
    -- TAB: STEAL AN EGG
    -- ==========================================
    local StealEggTab = Window:Tab({ Title = "Steal An Egg", Icon = "rbxassetid://10734898355" })

    StealEggTab:Button({
        Title = "Clouthub [NO KEY]",
        Description = "ESP, Egg Sniper Lock, Auto Grab",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ClouthubOnTop/Loader/main/main.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "YOKUDO HUB [NO KEY]",
        Description = "Farming, Combat, Auto Farm",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/betdoyvaka/stealanegg/main/Loader.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "CRZHub [NO KEY]",
        Description = "Auto Steal, Auto Hatch, Egg Prediction",
        Callback = function()
            loadstring(game:HttpGet("https://flowauth.net/v1/loaders/3c4e87ed34813171b0f8d53a108a7d88.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "Ouroboros Hub [NO KEY]",
        Description = "Auto Steal, Auto Hatch, Treadmill",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/joustingmatch/Ouroboros/main/loader.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "Valinc Hub [NO KEY]",
        Description = "Keyless Steal An Egg Script",
        Callback = function()
            loadstring(game:HttpGet("https://api.valincsyndicate.com/v1/releases/5502cba03703f4a3628d522d396b80d8.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "UB Hub [NO KEY]",
        Description = "Auto Steal, Pet Detection, Auto Hatch",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/TeamUBHub/UBLoader/refs/heads/main/Loader.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "Zero Point Hub [NO KEY]",
        Description = "Instant Steal, Anti Hit, Pet Detection",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/JaxRol/ZeroPoint/refs/heads/main/KeySystem"))()
        end,
    })

    StealEggTab:Button({
        Title = "Blyxo Hub [NO KEY]",
        Description = "Instant Steal, Auto Events",
        Callback = function()
            loadstring(game:HttpGet("https://flowauth.net/v1/loaders/69d3463240384f3a73fbe32c178093a2.lua"))()
        end,
    })

    StealEggTab:Button({
        Title = "Tsuo Hub [NO KEY]",
        Description = "Fast Steal, Auto Farm, Angel/Demon Eggs",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Tsuo7/TsuoHub/main/stealanegg"))()
        end,
    })

    -- ==========================================
    -- TAB: ADOPT ME
    -- ==========================================
    local AdoptMeTab = Window:Tab({ Title = "Adopt Me", Icon = "rbxassetid://10734898355" })

    AdoptMeTab:Button({
        Title = "House Cloner [NO KEY]",
        Description = "Clone any house instantly",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Vertex-Scripts/AdoptMe/main/HouseCloner.lua"))()
        end,
    })

    AdoptMeTab:Button({
        Title = "Axon Hub [NO KEY]",
        Description = "Auto Farm, Auto Collect, Pet ESP",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/AxonHub/AdoptMe/main/Axon.lua"))()
        end,
    })

    AdoptMeTab:Button({
        Title = "ZekeHub [KEY]",
        Description = "Auto Farm, Auto Neon, Money Farm (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ZekeHub/AdoptMe/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: BLADE BALL
    -- ==========================================
    local BladeBallTab = Window:Tab({ Title = "Blade Ball", Icon = "rbxassetid://10734898355" })

    BladeBallTab:Button({
        Title = "Dryx [NO KEY]",
        Description = "Auto Parry, Auto Block, Spam Parry",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/DryxScripts/BladeBall/main/Dryx.lua"))()
        end,
    })

    BladeBallTab:Button({
        Title = "SP Hub [NO KEY]",
        Description = "Auto Parry, Auto Clash, Auto Ability",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SPHub/BladeBall/main/SP.lua"))()
        end,
    })

    BladeBallTab:Button({
        Title = "ZekeHub [KEY]",
        Description = "Auto Parry, Auto Farm, Auto Win (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ZekeHub/BladeBall/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: PET SIMULATOR 99
    -- ==========================================
    local PS99Tab = Window:Tab({ Title = "Pet Simulator 99", Icon = "rbxassetid://10734898355" })

    PS99Tab:Button({
        Title = "6FootScripts [NO KEY]",
        Description = "Auto Farm, Auto Hatch, Auto Rank",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/6FootScripts/PS99/main/Loader.lua"))()
        end,
    })

    PS99Tab:Button({
        Title = "ZWARE [NO KEY]",
        Description = "Auto Farm, Auto Break, Auto Chest",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ZWARE/PS99/main/ZWARE.lua"))()
        end,
    })

    PS99Tab:Button({
        Title = "ZapHub [KEY]",
        Description = "Auto Farm, Auto Hatch, Auto Coins (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ZapHub/PS99/main/Loader.lua"))()
        end,
    })

    PS99Tab:Button({
        Title = "Forge Hub [KEY]",
        Description = "Auto Farm, Auto Hatch, Auto Event (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ForgeHub/PS99/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: MURDER MYSTERY 2
    -- ==========================================
    local MM2Tab = Window:Tab({ Title = "Murder Mystery 2", Icon = "rbxassetid://10734898355" })

    MM2Tab:Button({
        Title = "Aevryx [NO KEY]",
        Description = "ESP, Auto Shoot, Gun TP",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Aevryx/MM2/main/Loader.lua"))()
        end,
    })

    MM2Tab:Button({
        Title = "Vertex (MMV) [NO KEY]",
        Description = "ESP, Auto Shoot, Coin Farm",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Vertex-Scripts/MM2/main/MMV.lua"))()
        end,
    })

    MM2Tab:Button({
        Title = "SorinScript Hub [KEY]",
        Description = "Auto Farm, ESP, Auto Shoot (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SorinScript/MM2/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: THE STRONGEST BATTLEGROUNDS
    -- ==========================================
    local TSBTab = Window:Tab({ Title = "The Strongest Battlegrounds", Icon = "rbxassetid://10734898355" })

    TSBTab:Button({
        Title = "Kitty Ware [NO KEY]",
        Description = "Auto Block, Auto Dodge, Auto Attack",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/KittyWare/TSB/main/Loader.lua"))()
        end,
    })

    TSBTab:Button({
        Title = "KittyWare v2 [NO KEY]",
        Description = "Auto Block, Speed, Fly, Attack TP",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/KittyWare/TSB/main/v2.lua"))()
        end,
    })

    TSBTab:Button({
        Title = "VoidHunter [KEY]",
        Description = "Auto Block, Auto Dodge, Auto Combo (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/VoidHunter/TSB/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: DOORS
    -- ==========================================
    local DoorsTab = Window:Tab({ Title = "DOORS", Icon = "rbxassetid://10734898355" })

    DoorsTab:Button({
        Title = "Fragmented Mode v4 [NO KEY]",
        Description = "ESP, Auto Skip, God Mode",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Fragmented/DOORS/main/v4.lua"))()
        end,
    })

    DoorsTab:Button({
        Title = "ReefHub [NO KEY]",
        Description = "ESP, Auto Skip, Item ESP",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ReefHub/DOORS/main/Loader.lua"))()
        end,
    })

    DoorsTab:Button({
        Title = "99 Scripts [NO KEY]",
        Description = "99 keyless scripts collection",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/99Scripts/DOORS/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: GROW A GARDEN
    -- ==========================================
    local GrowGardenTab = Window:Tab({ Title = "Grow a Garden", Icon = "rbxassetid://10734898355" })

    GrowGardenTab:Button({
        Title = "DeltaScripts [NO KEY]",
        Description = "Auto Farm, Auto Plant, Auto Collect",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/DeltaScripts/GrowGarden/main/Loader.lua"))()
        end,
    })

    GrowGardenTab:Button({
        Title = "SorinScript Hub [KEY]",
        Description = "Auto Farm, Auto Plant, Auto Sell (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SorinScript/GrowGarden/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: BROOKHAVEN RP
    -- ==========================================
    local BrookhavenTab = Window:Tab({ Title = "Brookhaven RP", Icon = "rbxassetid://10734898355" })

    BrookhavenTab:Button({
        Title = "Voidware [NO KEY]",
        Description = "ESP, Fly, Speed, Teleport",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Voidware/Brookhaven/main/Loader.lua"))()
        end,
    })

    BrookhavenTab:Button({
        Title = "SorinScript Hub [KEY]",
        Description = "Auto Farm, ESP, Fly, Speed (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SorinScript/Brookhaven/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: ARSENAL
    -- ==========================================
    local ArsenalTab = Window:Tab({ Title = "Arsenal", Icon = "rbxassetid://10734898355" })

    ArsenalTab:Button({
        Title = "Synergy Hub [NO KEY]",
        Description = "Aimbot, ESP, Auto Shoot",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SynergyHub/Arsenal/main/Loader.lua"))()
        end,
    })

    ArsenalTab:Button({
        Title = "SorinScript Hub [KEY]",
        Description = "Aimbot, ESP, Auto Shoot, Wallbang (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SorinScript/Arsenal/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: VOXELS
    -- ==========================================
    local VoxelsTab = Window:Tab({ Title = "Voxels", Icon = "rbxassetid://10734898355" })

    VoxelsTab:Button({
        Title = "Kill Aura / God Mode [NO KEY]",
        Description = "Kill Aura, God Mode, Fly",
        Callback = function()
            loadstring(game:HttpGet("https://pastebin.com/raw/1bAGjw8j"))()
        end,
    })

    VoxelsTab:Button({
        Title = "Auto Place Blocks [NO KEY]",
        Description = "Auto Place Blocks, Auto Build",
        Callback = function()
            loadstring(game:HttpGet("https://pastebin.com/raw/1YtTES1r"))()
        end,
    })

    -- ==========================================
    -- TAB: BREAK A LUCKY BLOCK
    -- ==========================================
    local LuckyBlockTab = Window:Tab({ Title = "Break a Lucky Block", Icon = "rbxassetid://10734898355" })

    LuckyBlockTab:Button({
        Title = "GUMANBA [NO KEY]",
        Description = "Auto Break, Auto Collect, Auto Buy",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/gumanba/Scripts/main/BreakaLuckyBlock"))()
        end,
    })

    LuckyBlockTab:Button({
        Title = "KittyScripts [KEY]",
        Description = "Auto Break, Auto Collect, Auto Buy (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/KittyScripts/LuckyBlock/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: HYERSHOT
    -- ==========================================
    local HypershotTab = Window:Tab({ Title = "Hypershot", Icon = "rbxassetid://10734898355" })

    HypershotTab:Button({
        Title = "sel01 Hub [NO KEY]",
        Description = "Aimbot, ESP, Auto Shoot",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/seltonmt012/sel01-rbx/main/loader.lua"))()
        end,
    })

    HypershotTab:Button({
        Title = "Hitbox Expander [NO KEY]",
        Description = "Hitbox Expander, Aimbot",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Hypershot/Hitbox/main/Loader.lua"))()
        end,
    })

    HypershotTab:Button({
        Title = "Snowy Hub [KEY]",
        Description = "Aimbot, ESP, Auto Shoot (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/SnowyHub/Hypershot/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: BUILD AN AI
    -- ==========================================
    local BuildAITab = Window:Tab({ Title = "Build an AI", Icon = "rbxassetid://10734898355" })

    BuildAITab:Button({
        Title = "Ouroboros [NO KEY]",
        Description = "Auto Build, Auto Farm, Auto Collect",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/joustingmatch/Ouroboros/main/loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: RUNAWAYS
    -- ==========================================
    local RunawaysTab = Window:Tab({ Title = "RUNAWAYS", Icon = "rbxassetid://10734898355" })

    RunawaysTab:Button({
        Title = "28 Keyless Scripts [NO KEY]",
        Description = "Collection of 28 keyless scripts",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Rscripts/RUNAWAYS/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: MULTICREW TANK COMBAT
    -- ==========================================
    local MTCTab = Window:Tab({ Title = "Multicrew Tank Combat", Icon = "rbxassetid://10734898355" })

    MTCTab:Button({
        Title = "14 Keyless Scripts [NO KEY]",
        Description = "Collection of 14 keyless scripts",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Rscripts/MTC/main/Loader.lua"))()
        end,
    })

    -- ==========================================
    -- TAB: UNIVERSAL
    -- ==========================================
    local UniversalTab = Window:Tab({ Title = "Universal", Icon = "rbxassetid://10734898355" })

    UniversalTab:Button({
        Title = "Hawk's Hub [NO KEY]",
        Description = "Fly, NoClip, Speed, Infinite Jump",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/HawksHub/Universal/main/Loader.lua"))()
        end,
    })

    UniversalTab:Button({
        Title = "Universal Fly & NoClip [NO KEY]",
        Description = "Fly, NoClip, Speed",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Universal/FlyNoClip/main/Loader.lua"))()
        end,
    })

    UniversalTab:Button({
        Title = "ROXCOM Emotes [NO KEY]",
        Description = "All emotes unlocked",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/ROXCOM/Emotes/main/Loader.lua"))()
        end,
    })

    UniversalTab:Button({
        Title = "Universal Hitbox Extender [KEY]",
        Description = "Hitbox Extender, Aimbot (Key: tony)",
        Callback = function()
            loadstring(game:HttpGet("https://raw.githubusercontent.com/Universal/Hitbox/main/Loader.lua"))()
        end,
    })

    -- Startup notification
    WindUI:Notify({
        Title = "Tony's Hub",
        Content = "GUI loaded! 18 game tabs available.",
        Duration = 5,
    })

end
