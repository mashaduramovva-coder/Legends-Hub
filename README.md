"if not game:IsLoaded() then
    repeat task.wait() until game:IsLoaded()
end

if setfpscap then
    setfpscap(1000000)
    game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Black Hub",
        Text = "FPS Unlocked!",
        Duration = 5,
        Button1 = "Okay"
    })
    warn("FPS Unlocked!")
else
    game:GetService("StarterGui"):SetCore("SendNotification", {
        Title = "Black Hub",
        Text = "Your exploit does not support setfpscap.",
        Duration = 5,
        Button1 = "Okay"
    })
    warn("Your exploit does not support setfpscap.")
end

local WindUI = (loadstring(game:HttpGet("https://github.com/Footagesus/WindUI/releases/latest/download/main.lua")))();
local Window = WindUI:CreateWindow({
    Title = "Black Hub",
    Icon = "rbxassetid://84228153855933",
    Author = "Black Hub | Blox Fruit",
    Folder = "Bkack Hub_BF",
    Size = UDim2.fromOffset(550, 300),
    Transparent = true,
    Theme = "Dark",
    SideBarWidth = 190,
    HasOutline = false,
    HideSearchBar = true,
    ScrollBarEnabled = false,
    User = {
        Enabled = true,
        Anonymous = false
    },
});
Window:EditOpenButton({
    Title = "Black Hub- Open",
    Icon = "monitor",
    CornerRadius = UDim.new(0, 6),
    StrokeThickness = 2,
    Color = ColorSequence.new(Color3.fromRGB(30, 30, 30), Color3.fromRGB(255, 255, 255)),
    Draggable = true
});
local Tabs = {
    InfoTab = Window:Tab({
        Title = "Information",
        Icon = "info",
        Desc = "Info Section"
    }),
    MainDivider = Window:Divider(),
    MainTab = Window:Tab({
        Title = "Farming",
        Icon = "rocket",
        Desc = "Main Section"
    }),
    OthersTab = Window:Tab({
        Title = "Others",
        Icon = "crown",
        Desc = "Farming Section"
    }),
    ItemsTab = Window:Tab({
        Title = "Items",
        Icon = "box",
        Desc = "Items Section"
    }),
    SettingsTab = Window:Tab({
        Title = "Settings",
        Icon = "settings",
        Desc = "Settings Section"
    }),
    PlayerDivider = Window:Divider(),
    LocalPlayerTab = Window:Tab({
        Title = "Player",
        Icon = "user",
        Desc = "Local Player Section"
    }),
    StatsTab = Window:Tab({
        Title = "Stats",
        Icon = "sliders-horizontal",
        Desc = "Stats Section"
    }),
    SeaDivider = Window:Divider(),
    SeaEventTab = Window:Tab({
        Title = "Sea Event",
        Icon = "anchor",
        Desc = "Sea Event Section"
    }),
    SeaStackTab = Window:Tab({
        Title = "Sea Stack",
        Icon = "waves",
        Desc = "Sea Stack Section"
    }),
    SeaSettingsTab = Window:Tab({
        Title = "Sea Settings",
        Icon = "cog",
        Desc = "Sea Settings Section"
    }),
    AutoDivider = Window:Divider(),
    DragonDojoTab = Window:Tab({
        Title = "Dragon Dojo",
        Icon = "shield",
        Desc = "Dragon Dojo Section"
    }),
    RaceTab = Window:Tab({
        Title = "Race V4",
        Icon = "bot",
        Desc = "Race Section"
    }),
    CombatDivider = Window:Divider(),
    CombatTab = Window:Tab({
        Title = "Combat",
        Icon = "sword",
        Desc = "Combat Section"
    }),
    RaidTab = Window:Tab({
        Title = "Raid",
        Icon = "door-open",
        Desc = "Raid Section"
    }),
    EspTab = Window:Tab({
        Title = "Esp",
        Icon = "eye",
        Desc = "Esp Section"
    }),
    TeleportTab = Window:Tab({
        Title = "Teleport",
        Icon = "map-pinned",
        Desc = "Teleport Section"
    }),
    ShopTab = Window:Tab({
        Title = "Shop",
        Icon = "shopping-cart",
        Desc = "Shop Section"
    }),
    FruitTab = Window:Tab({
        Title = "Fruit",
        Icon = "apple",
        Desc = "Fruit Section"
    }),
    MiscDivider = Window:Divider(),
    MiscTab = Window:Tab({
        Title = "Misc",
        Icon = "layout-grid",
        Desc = "Misc Section"
    }),
    ServerTab = Window:Tab({
        Title = "Server",
        Icon = "server",
        Desc = "Server Section"
    })
};
Window:SelectTab(1);
_G.Settings = {
    Main = {
        ["Select Weapon"] = "Melee",
        ["Farm Level Method"] = "Quest",
        ["Auto Farm"] = false,
        ["Auto Fast Farm"] = false,
        ["Mastery Method"] = "Quest",
        ["Auto Farm Fruit Mastery"] = false,
        ["Auto Farm Gun Mastery"] = false,
        ["Selected Mastery Sword"] = nil,
        ["Auto Farm Sword Mastery"] = false,
        ["Auto Summon Tyrant Of The Skies"] = false,
        ["Auto Kill Tyrant Of The Skies"] = false,
        ["Selected Mon"] = nil,
        ["Auto Farm Mon"] = false,
        ["Selected Boss"] = nil,
        ["Auto Farm Boss"] = false,
        ["Auto Farm All Boss"] = false
    },
    Event = {},
    Farm = {
        ["Auto Elite Hunter"] = false,
        ["Auto Elite Hunter Hop"] = false,
        ["Selected Bone Farm Method"] = "Quest",
        ["Auto Farm Bone"] = false,
        ["Auto Random Surprise"] = false,
        ["Auto Pirate Raid"] = false,
        ["Auto Farm Chest Tween"] = false,
        ["Auto Farm Chest Instant"] = false,
        ["Auto Chest Hop"] = false,
        ["Auto Farm Chest Mirage"] = false,
        ["Auto Stop Items"] = false,
        ["Auto Farm Katakuri"] = false,
        ["Auto Spawn Cake Prince"] = false,
        ["Auto Kill Cake Prince"] = false,
        ["Auto Kill Dough King"] = false,
        ["Selected Material"] = nil,
        ["Auto Farm Material"] = false
    },
    Setting = {
        ["Spin Position"] = false,
        ["Farm Distance"] = 35,
        ["Player Tween Speed"] = 350,
        ["Bring Mob"] = true,
        ["Bring Mob Mode"] = "Normal",
        ["Fast Attack"] = true,
        ["Fast Attack Mode"] = "Normal",
        ["Attack Aura"] = true,
        ["Hide Notification"] = false,
        ["Hide Damage Text"] = true,
        ["Black Screen"] = false,
        ["White Screen"] = false,
        ["Hide Monster"] = false,
        ["Mastery Health"] = 25,
        ["Fruit Mastery Skill Z"] = true,
        ["Fruit Mastery Skill X"] = true,
        ["Fruit Mastery Skill C"] = true,
        ["Fruit Mastery Skill V"] = false,
        ["Fruit Mastery Skill F"] = false,
        ["Gun Mastery Skill Z"] = true,
        ["Gun Mastery Skill X"] = true,
        ["Auto Set Spawn Point"] = true,
        ["Auto Observation"] = false,
        ["Auto Haki"] = true,
        ["Auto Rejoin"] = true
    },
    Stats = {
        ["Auto Add Melee Stats"] = false,
        ["Auto Add Defense Stats"] = false,
        ["Auto Add Devil Fruit Stats"] = false,
        ["Auto Add Sword Stats"] = false,
        ["Auto Add Gun Stats"] = false,
        ["Point Stats"] = 1
    },
    Items = {
        ["Auto Second Sea"] = false,
        ["Auto Third Sea"] = false,
        ["Auto Farm Factory"] = false,
        ["Auto Super Human"] = false,
        ["Auto Death Step"] = false,
        ["Auto Fishman Karate"] = false,
        ["Auto Electric Claw"] = false,
        ["Auto Dragon Talon"] = false,
        ["Auto God Human"] = false,
        ["Auto Saber"] = false,
        ["Auto Buddy Sword"] = false,
        ["Auto Soul Guitar"] = false,
        ["Auto Rengoku"] = false,
        ["Auto Hallow Scythe"] = false,
        ["Auto Warden Sword"] = false,
        ["Auto Cursed Dual Katana"] = false,
        ["Auto Yama"] = false,
        ["Auto Tushita"] = false,
        ["Auto Canvander"] = false,
        ["Auto Dragon Trident"] = false,
        ["Auto Pole"] = false,
        ["Auto Shawk Saw"] = false,
        ["Auto Greybeard"] = false,
        ["Auto Swan Glasses"] = false,
        ["Auto Arena Trainer"] = false,
        ["Auto Dark Dagger"] = false,
        ["Auto Press Haki Button"] = false,
        ["Auto Rainbow Haki"] = false,
        ["Auto Holy Torch"] = false,
        ["Auto Bartilo Quest"] = false
    },
    Esp = {
        ["ESP Player"] = false,
        ["ESP Chest"] = false,
        ["ESP DevilFruit"] = false,
        ["ESP RealFruit"] = false,
        ["ESP Flower"] = false,
        ["ESP Island"] = false,
        ["ESP Npc"] = false,
        ["ESP Sea Beast"] = false,
        ["ESP Monster"] = false,
        ["ESP Mirage"] = false,
        ["ESP Kitsune"] = false,
        ["ESP Frozen"] = false,
        ["ESP Advanced Fruit Dealer"] = false,
        ["ESP Aura"] = false,
        ["ESP Gear"] = false
    },
    DragonDojo = {
        ["Auto Farm Blaze Ember"] = false,
        ["Auto Collect Blaze Ember"] = false
    },
    SeaEvent = {
        ["Selected Boat"] = "Guardian",
        ["Selected Zone"] = "Zone 5",
        ["Boat Tween Speed"] = 300,
        ["Sail Boat"] = false,
        ["Auto Farm Shark"] = true,
        ["Auto Farm Piranha"] = true,
        ["Auto Farm Fish Crew Member"] = true,
        ["Auto Farm Ghost Ship"] = true,
        ["Auto Farm Pirate Brigade"] = true,
        ["Auto Farm Pirate Grand Brigade"] = true,
        ["Auto Farm Terrorshark"] = true,
        ["Auto Farm Seabeasts"] = true,
        ["Dodge Seabeasts Attack"] = true,
        ["Dodge Terrorshark Attack"] = true
    },
    SettingSea = {
        Lightning = false,
        ["Increase Boat Speed"] = false,
        ["No Clip Rock"] = false,
        ["Use Devil Fruit Skill"] = true,
        ["Use Melee Skill"] = true,
        ["Use Sword Skill"] = true,
        ["Use Gun Skill"] = true,
        ["Devil Fruit Z Skill"] = true,
        ["Devil Fruit X Skill"] = true,
        ["Devil Fruit C Skill"] = true,
        ["Devil Fruit V Skill"] = false,
        ["Devil Fruit F Skill"] = false,
        ["Melee Z Skill"] = true,
        ["Melee X Skill"] = true,
        ["Melee C Skill"] = true,
        ["Melee V Skill"] = true
    },
    SeaStack = {
        ["Tween To Frozen Dimension"] = false,
        ["Summon Frozen Dimension"] = false,
        ["Tween To Kitsune Island"] = false,
        ["Summon Kitsune Island"] = false,
        ["Auto Collect Azure Ember"] = false,
        ["Set Azure Ember"] = 20,
        ["Auto Trade Azure Ember"] = false,
        ["Tween To Mirage Island"] = false,
        ["Teleport To Advanced Fruit Dealer"] = false,
        ["Auto Attack Seabeasts"] = false,
        ["Summon Prehistoric Island"] = false,
        ["Tween To Prehistoric Island"] = false,
        ["Auto Kill Lava Golem"] = false
    },
    Race = {
        ["Auto Race V2"] = false,
        ["Auto Race V3"] = false,
        ["Selected Place"] = nil,
        ["Teleport To Place"] = false,
        ["Auto Buy Gear"] = false,
        ["Tween To Highest Mirage"] = false,
        ["Find Blue Gear"] = false,
        ["Look Moon Ability"] = false,
        ["Auto Train"] = false,
        ["Auto Kill Player After Trial"] = false,
        ["Auto Trial"] = false
    },
    Combat = {
        ["Auto Kill Player Quest"] = false,
        ["Aimbot Gun"] = false,
        ["Aimbot Skill Neares"] = false,
        ["Aimbot Skill"] = false,
        ["Enable PvP"] = false
    },
    Raid = {
        ["Selected Chip"] = nil,
        ["Auto Raid"] = false,
        ["Auto Awaken"] = false,
        ["Price Devil Fruit"] = 1000000,
        ["Unstore Devil Fruit"] = false,
        ["Law Raid"] = false
    },
    Shop = {
        ["Auto Buy Legendary Sword"] = false,
        ["Auto Buy Haki Color"] = false
    },
    LocalPlayer = {
        ["Infinite Energy"] = false,
        ["Infinite Ability"] = true,
        ["Infinite Geppo"] = false,
        ["Infinite Soru"] = false,
        ["Dodge No Cooldown"] = false,
        ["Active Race V3"] = false,
        ["Active Race V4"] = true,
        ["Walk On Water"] = true,
        ["No Clip"] = false
    },
    Fruit = {
        ["Auto Buy Random Fruit"] = false,
        ["Store Rarity Fruit"] = "Common - Mythical",
        ["Auto Store Fruit"] = false,
        ["Fruit Notification"] = false,
        ["Teleport To Fruit"] = false,
        ["Tween To Fruit"] = false
    },
    Misc = {
        ["Hide Chat"] = false,
        ["Hide Leaderboard"] = false,
        ["Highlight Mode"] = false
    }
};
(getgenv()).Load = function()
    if readfile and writefile and isfile and isfolder then
        if not isfolder("Relz Hub New") then
            makefolder("Relz Hub New");
        end
        if not isfolder("Relz Hub New/Blox Fruits/") then
            makefolder("Relz Hub New/Blox Fruits/");
        end
        if not isfile(("Relz Hub New/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json")) then
            writefile("Relz Hub New/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json",
                (game:GetService("HttpService")):JSONEncode(_G.Settings));
        else
            local Decode = (game:GetService("HttpService")):JSONDecode(readfile(
                "Relz Hub New/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json"));
            for i, v in pairs(Decode) do
                _G.Settings[i] = v;
            end
        end
        print("Loaded!");
    else
        return warn("Status : Undetected Executor");
    end
end;
(getgenv()).SaveSetting = function()
    if readfile and writefile and isfile and isfolder then
        if not isfile(("Relz Hub New/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json")) then
            (getgenv()).Load();
        else
            local Decode = (game:GetService("HttpService")):JSONDecode(readfile(
                "Relz Hub New/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json"));
            local Array = {};
            for i, v in pairs(_G.Settings) do
                Array[i] = v;
            end
            writefile("Relz Hub New/Blox Fruits/" .. game.Players.LocalPlayer.Name .. ".json",
                (game:GetService("HttpService")):JSONEncode(Array));
        end
    else
        return warn("Status : Undetected Executor");
    end
end;
(getgenv()).Load();
if game.PlaceId == 2753915549 then
    World1 = true;
elseif game.PlaceId == 4442272183 then
    World2 = true;
elseif game.PlaceId == 7449423635 then
    World3 = true;
end
function CheckQuest()
    MyLevel = (game:GetService("Players")).LocalPlayer.Data.Level.Value;
    if World1 then
        if MyLevel == 1 or MyLevel <= 9 then
            Mon = "Bandit";
            LevelQuest = 1;
            NameQuest = "BanditQuest1";
            NameMon = "Bandit";
            CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231, 0.939700544, -0, -0.341998369, 0, 1, -0,
                0.341998369, 0, 0.939700544);
            CFrameMon = CFrame.new(1045.962646484375, 27.00250816345215, 1560.8203125);
        elseif MyLevel == 10 or MyLevel <= 14 then
            Mon = "Monkey";
            LevelQuest = 1;
            NameQuest = "JungleQuest";
            NameMon = "Monkey";
            CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0);
            CFrameMon = CFrame.new(-1448.51806640625, 67.85301208496094, 11.46579647064209);
        elseif MyLevel == 15 or MyLevel <= 29 then
            Mon = "Gorilla";
            LevelQuest = 2;
            NameQuest = "JungleQuest";
            NameMon = "Gorilla";
            CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0);
            CFrameMon = CFrame.new(-1129.8836669921875, 40.46354675292969, -525.4237060546875);
        elseif MyLevel == 30 or MyLevel <= 39 then
            Mon = "Pirate";
            LevelQuest = 1;
            NameQuest = "BuggyQuest1";
            NameMon = "Pirate";
            CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0,
                0.258804798, 0, 0.965929627);
            CFrameMon = CFrame.new(-1103.513427734375, 13.752052307128906, 3896.091064453125);
        elseif MyLevel == 40 or MyLevel <= 59 then
            Mon = "Brute";
            LevelQuest = 2;
            NameQuest = "BuggyQuest1";
            NameMon = "Brute";
            CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0,
                0.258804798, 0, 0.965929627);
            CFrameMon = CFrame.new(-1140.083740234375, 14.809885025024414, 4322.92138671875);
        elseif MyLevel == 60 or MyLevel <= 74 then
            Mon = "Desert Bandit";
            LevelQuest = 1;
            NameQuest = "DesertQuest";
            NameMon = "Desert Bandit";
            CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0,
                0.573571265, 0, 0.819155693);
            CFrameMon = CFrame.new(924.7998046875, 6.44867467880249, 4481.5859375);
        elseif MyLevel == 75 or MyLevel <= 89 then
            Mon = "Desert Officer";
            LevelQuest = 2;
            NameQuest = "DesertQuest";
            NameMon = "Desert Officer";
            CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0,
                0.573571265, 0, 0.819155693);
            CFrameMon = CFrame.new(1608.2822265625, 8.614224433898926, 4371.00732421875);
        elseif MyLevel == 90 or MyLevel <= 99 then
            Mon = "Snow Bandit";
            LevelQuest = 1;
            NameQuest = "SnowQuest";
            NameMon = "Snow Bandit";
            CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0,
                -0.939684391, 0, -0.342042685);
            CFrameMon = CFrame.new(1354.347900390625, 87.27277374267578, -1393.946533203125);
        elseif MyLevel == 100 or MyLevel <= 119 then
            Mon = "Snowman";
            LevelQuest = 2;
            NameQuest = "SnowQuest";
            NameMon = "Snowman";
            CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0,
                -0.939684391, 0, -0.342042685);
            CFrameMon = CFrame.new(1201.6412353515625, 144.57958984375, -1550.0670166015625);
        elseif MyLevel == 120 or MyLevel <= 149 then
            Mon = "Chief Petty Officer";
            LevelQuest = 1;
            NameQuest = "MarineQuest2";
            NameMon = "Chief Petty Officer";
            CFrameQuest = CFrame.new(-5039.58643, 27.3500385, 4324.68018, 0, 0, -1, 0, 1, 0, 1, 0, 0);
            CFrameMon = CFrame.new(-4881.23095703125, 22.65204429626465, 4273.75244140625);
        elseif MyLevel == 150 or MyLevel <= 174 then
            Mon = "Sky Bandit";
            LevelQuest = 1;
            NameQuest = "SkyQuest";
            NameMon = "Sky Bandit";
            CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0,
                -0.500031412, 0, 0.866007268);
            CFrameMon = CFrame.new(-4953.20703125, 295.74420166015625, -2899.22900390625);
        elseif MyLevel == 175 or MyLevel <= 189 then
            Mon = "Dark Master";
            LevelQuest = 2;
            NameQuest = "SkyQuest";
            NameMon = "Dark Master";
            CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0,
                -0.500031412, 0, 0.866007268);
            CFrameMon = CFrame.new(-5259.8447265625, 391.3976745605469, -2229.035400390625);
        elseif MyLevel == 190 or MyLevel <= 209 then
            Mon = "Prisoner";
            LevelQuest = 1;
            NameQuest = "PrisonerQuest";
            NameMon = "Prisoner";
            CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514, -0.0894274712, -0.00000000500292918,
                -0.995993316, 0.00000000160817859, 1, -0.00000000516744869, 0.995993316, -0.00000000206384709,
                -0.0894274712);
            CFrameMon = CFrame.new(5098.9736328125, -0.3204058110713959, 474.2373352050781);
        elseif MyLevel == 210 or MyLevel <= 249 then
            Mon = "Dangerous Prisoner";
            LevelQuest = 2;
            NameQuest = "PrisonerQuest";
            NameMon = "Dangerous Prisoner";
            CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514, -0.0894274712, -0.00000
