--_G.AutoFarm = "" --Hoop/Orb
if not game:IsLoaded() then game.Loaded:Wait() end
if game.PlaceId ~= 3101667897 then return end

local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/garnoog/Guia/main/README.md" , true))()
local win = library:CreateWindow({Name = "Dummy Hub [ Legends Of Speed ⚡ ]",Themeable = {info = "Doing by Dummy"}})

local General_Tab = win:Tab("General"),Enum.KeyCode.RightControl
local M = General_Tab:CreateSection("info")
local St = M:AddLabel("🟢Start🟢")
spawn(function()
while wait() do
St:Set("🔵Start🔵")
wait(1)
St:Set("🟣Start🟣")
wait(1)
St:Set("🔴Start🔴")
wait(1)
St:Set("🟠Start🟠")
wait(1)
St:Set("🟡Start🟡")
wait(1)
St:Set("🟢Start🟢")
end
end)

local Status = General_Tab:CreateSection({"Status"})
local Rebirth_C = Status:AddLabel("Rebirth      : 0")
local Level_C =   Status:AddLabel("Level        : 0")
local Races_C =   Status:AddLabel("Races        : 0")
local Gem_C =     Status:AddLabel("Gem          : 0")
local Step_C =    Status:AddLabel("Step         : 0")
local W_C =       Status:AddLabel("Your Land    : ")
local R_C =       Status:AddLabel("Your Rank   : ")

local wr = General_Tab:CreateSection("World Ready")
local gc = wr:AddLabel("🔴 : Grass Course") --lv 5-
local mc = wr:AddLabel("🔴 : Mysterious Cave") --lv 25-
local os = wr:AddLabel("🔴 : Outer Space") --race 50-
local pk = wr:AddLabel("🔴 : Parkour") --lv 35-
local fc = wr:AddLabel("🔴 : Frost Course") --lv 15-
local ifc = wr:AddLabel("🔴 : Inferno Cave") --re 1-
local pc = wr:AddLabel("🔴 : Pirate Course") --lv 50-

local RC = General_Tab:CreateSection({Name = "Random Cabinet",Side = "Right"})
local Yc =   RC:AddLabel("🔴 : Yellow Crystal") --1,200-
local Pc =   RC:AddLabel("🔴 : Purple Crystal") --1,000-
local Lc =   RC:AddLabel("🔴 : Lava Crystal") --8,000-
local ELc =  RC:AddLabel("🔴 : Electro Legends Crystal") --100,000-
local IFNc = RC:AddLabel("🔴 : Inferno Crystal") --8,000-
local SNc = RC:AddLabel("🔴 : Snow Crystal") --4,000-
local LNc = RC:AddLabel("🔴 : Lightning Crystal") --2,500-
local Bc = RC:AddLabel("🔴 : Blue Crystal") --600-
local Rc = RC:AddLabel("🔴 : Red Crystal") --300-

spawn(function()
    while wait() do
        pcall(function()
                local Gem = game:GetService("Players").LocalPlayer.Gems.Value
                if Gem >= 600 then
        Bc:Set("🟢 : Blue Crystal")
        else
        Bc:Set("🔴 : Blue Crystal")
    end
    if Gem >= 300 then
        Rc:Set("🟢 : Red Crystal")
        else
        Rc:Set("🔴 : Red Crystal")
    end
    if Gem >= 1000 then
        Pc:Set("🟢 : Purple Crystal")
        else
        Pc:Set("🔴 : Purple Crystal")
    end
    if Gem >= 1200 then
        Yc:Set("🟢 : Yellow Crystal")
        else
        Yc:Set("🔴 : Yellow Crystal")
    end
    if Gem >= 8000 then
        Lc:Set("🟢 : Lava Crystal")
        else
        Lc:Set("🔴 : Lava Crystal")
    end
    if Gem >= 8000 then
        IFNc:Set("🟢 : Inferno Crystal")
        else
        IFNc:Set("🔴 : Inferno Crystal") 
    end
    if Gem >= 2500 then
        LNc:Set("🟢 : Lightning Crystal")
        else
        LNc:Set("🔴 : Lightning Crystal")
    end
    if Gem >= 4000 then
        SNc:Set("🟢 : Snow Crystal")
        else
        SNc:Set("🔴 : Snow Crystal")
    end
    if Gem >= 100000 then
        ELc:Set("🟢 : Electro Legends Crystal")
        else
        ELc:Set("🔴 : Electro Legends Crystal")
    end
    
    local lv = game:GetService("Players").LocalPlayer.level.Value
    if lv >= 5 then
        gc:Set("🟢 : Grass Course")
        else
        gc:Set("🔴 : Grass Course")
    end
    if lv >= 25 then
        mc:Set("🟢 : Mysterious Cave")
        else
        mc:Set("🔴 : Mysterious Cave")
    end
    if lv >= 35 then
        pk:Set("🟢 : Parkour")
        else
        pk:Set("🔴 : Parkour")
    end
    if lv >= 15 then
        fc:Set("🟢 : Frost Course")
        else
        fc:Set("🔴 : Frost Course")
    end
    if lv >= 50 then
        pc:Set("🟢 : Pirate Course")
        else
        pc:Set("🔴 : Pirate Course")
    end
    
        end)
    end
    end)

spawn(function()
    local rb = game:GetService("Players").LocalPlayer.leaderstats.Rebirths.Value
    if rb >= 1 then
        ifc:Set("🟢 : Inferno Cave")
        else
        ifc:Set("🔴 : Inferno Cave")
    end
    end)


spawn(function()
    local r = game:GetService("Players").LocalPlayer.leaderstats.Races.Value
    if r >= 50 then
        os:Set("🟢 : Outer Space")
        else
        os:Set("🔴 : Outer Space")
    end
    
    if r <= 1 then
        R_C:Set("Your Rank   : RooKie")
    elseif r == 1 or r <= 4 then
        R_C:Set("Your Rank   : Runner")
    elseif r == 5 or r <= 9 then
        R_C:Set("Your Rank   : Hyper")
    elseif r == 10 or r <= 19 then
        R_C:Set("Your Rank   : Racer")
    elseif r == 20 or r <= 29 then
        R_C:Set("Your Rank   : Hot Rod")
    elseif r == 30 or r <= 49 then
        R_C:Set("Your Rank   : Lightning")
    elseif r == 50 or r <= 79 then
        R_C:Set("Your Rank   : Pro Circuit")
    elseif r == 80 or r <= 119 then
        R_C:Set("Your Rank   : Master Racer")
    elseif r == 120 or r <= 199 then
        R_C:Set("Your Rank   : Legendary")
    elseif r >= 200 then
        R_C:Set("Your Rank   : Legendary")
        end
    end)
-- 🟢
-- 🔴
spawn(function()
	while wait() do
		pcall(function()
			CheckStat()
		end)
	end
end)
function CheckStat()
          W_C:Set("Your Land   : "..tostring(game:GetService("Players").LocalPlayer.currentMap.Value))
    Rebirth_C:Set("Rebirth     : "..tostring(game:GetService("Players").LocalPlayer.leaderstats.Rebirths.Value))
      Level_C:Set("Level       : "..tostring(game:GetService("Players").LocalPlayer.level.Value))
      Races_C:Set("Races       : "..tostring(game:GetService("Players").LocalPlayer.leaderstats.Races.Value))
        Gem_C:Set("Gem         : "..tostring(game:GetService("Players").LocalPlayer.Gems.Value))
       Step_C:Set("Step        : "..tostring(game:GetService("Players").LocalPlayer.leaderstats.Steps.Value))
end
    

local Rd = General_Tab:CreateSection({Name = "Random",Side = "Right"})
Rd:AddButton({
    Name = "Red [300 gem]",
    Callback = function()
    -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Red Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Blue [600 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Blue Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Purple [1,000 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Purple Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Yellow [1,200 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Yellow Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Lightning [2,500 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Lightning Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Snow [4,000 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Snow Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Inferno [8,000 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Inferno Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Lava [8,000 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Lava Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})
Rd:AddButton({
    Name = "Electro Legends [100,000 gem]",
    Callback = function()
        -- Script generated by SimpleSpy - credits to exx#9394

local args = {
    [1] = "openCrystal",
    [2] = "Electro Legends Crystal"
}

game:GetService("ReplicatedStorage").rEvents.openCrystalRemote:InvokeServer(unpack(args))

        end
})

spawn( 
    function()
        if _G.AutoFarm == "Orb" then
        while task.wait() do
                game:GetService("ReplicatedStorage").rEvents.rebirthEvent:FireServer("rebirthRequest")
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Red Orb", "City")
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Gem", "City")
                game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City") game:GetService('ReplicatedStorage').rEvents.orbEvent:FireServer("collectOrb", "Yellow Orb", "City")
        end
    end
end)
spawn(
    function()
        if _G.AutoFarm == "Hoop" then
            while wait() do
                for i,v in pairs(game:GetService("Workspace").Hoops:GetChildren()) do
				firetouchinterest(v, game:GetService('Players').LocalPlayer.Character.HumanoidRootPart, 0)
				wait()
				firetouchinterest(v, game:GetService('Players').LocalPlayer.Character.HumanoidRootPart, 1)
				local children = workspace.Hoops:GetChildren()
                    for i, child in ipairs(children) do
                        if child.Name == "Hoop" then
                        child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                end
            end
				end
        end
            end
    end)
