--1tsJusthub V2 lite for Arcerus X

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("1tsJusthub Lite (for Arcerus X)", "DarkTheme")

local Main = Window:NewTab("Main")
local MainSection = Main:NewSection("Main")

    MainSection:NewDropdown("Gun", "Give U Gun", {"M9", "Remington 870", "AK-47"}, function(v)
    local A_1 = game:GetService("Workspace")["Prison_ITEMS"].giver[v].ITEMPICKUP
        local Event = game:GetService("Workspace").Remote.ItemHandler
        Event:InvokeServer(A_1)
end)

MainSection:NewButton("Give Weapon", "Give u Hammer and Knife", function()
    local A_1 = game:GetService("Workspace")["Prison_ITEMS"].single["Crude Knife"].ITEMPICKUP
local Event = game:GetService("Workspace").Remote.ItemHandler
Event:InvokeServer(A_1)

wait(0.5)

local A_1 = game:GetService("Workspace")["Prison_ITEMS"].single.Hammer.ITEMPICKUP
local Event = game:GetService("Workspace").Remote.ItemHandler
Event:InvokeServer(A_1)
end)

MainSection:NewButton("KeyCard", "Give U KeyCard", function()
    local A_1 = game:GetService("Workspace")["Prison_ITEMS"].single["Key card"].ITEMPICKUP
    local Event = game:GetService("Workspace").Remote.ItemHandler
    Event:InvokeServer(A_1)
end)

MainSection:NewButton("Infinity yield", "Infinity yield", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

MainSection:NewButton("Btools", "Give U Btools", function()
    local tool3 = Instance.new("HopperBin",game.Players.LocalPlayer.Backpack)
    tool3.BinType = "Hammer"
end)

--Localplayer









local LocalPlayer = Window:NewTab("LocalPlayer")
local LocalPlayerSection = LocalPlayer:NewSection("LocalPlayer")
LocalPlayerSection:NewSlider("Walkspeed", "Cambia La tua velocita", 500, 16, function(v)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
end)
LocalPlayerSection:NewSlider("Jumppower", "Fai u cunighiu", 500, 50, function(v)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
end)

LocalPlayerSection:NewButton("Infinite Jump", "Infinite Jump", function()
    local Player = game:GetService'Players'.LocalPlayer;
local UIS = game:GetService'UserInputService';

_G.JumpHeight = 50;

function Action(Object, Function) if Object ~= nil then Function(Object); end end

UIS.InputBegan:connect(function(UserInput)
if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.Space then
    Action(Player.Character.Humanoid, function(self)
        if self:GetState() == Enum.HumanoidStateType.Jumping or self:GetState() == Enum.HumanoidStateType.Freefall then
            Action(self.Parent.HumanoidRootPart, function(self)
                self.Velocity = Vector3.new(0, _G.JumpHeight, 0);
            end)
        end
    end)
end
end)
end)

    --Chat Spam















    local Main = Window:NewTab("Chat")
    local ChatSection = Main:NewSection("Chat Spam")

    ChatSection:NewButton("Chat Spam", "Chat Spam", function()
        local Insults = {"1tsJustHub v2 Lite (for Arcerus X)", " 1tsJustHub Lite (For Arcerus X) is Cool", "Credit 1tsJustgp", "1tsJustHub is the best hub", "Very op Script", "gp1tsJust#3203", "search on yt 1tsJustgp", "For Get It!"}

spawn(function()
    while true do
        game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(Insults[math.random(1,#Insults)], "All")
        task.wait(1)
    end
end)
    end)

    --TP










    

    local Main = Window:NewTab("Teleport")
    local TPSection = Main:NewSection("Teleport")

    TPSection:NewButton("Prison", "Tp to prison", function()
        local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(914, 99, 2377)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
wait(0.1)
pl.CFrame = location
    end)

    TPSection:NewButton("Yard", "Tp to Yard", function()
        local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(780, 97, 2461)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
wait(0.1)
pl.CFrame = location
    end)

    TPSection:NewButton("Criminal Base", "TP to Criminal Base", function()
        local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(-943, 94, 2064)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
wait(0.1)
pl.CFrame = location
    end)

    TPSection:NewButton("Police Base", "TP to Police Base", function()
        local pl = game.Players.LocalPlayer.Character.HumanoidRootPart
local location = CFrame.new(834, 99, 2303)
local humanoid = game.Players.LocalPlayer.Character.Humanoid
wait(0.1)
pl.CFrame = location
    end)


        --Credit

    local Main = Window:NewTab("Credit")
    local Credit2Section = Main:NewSection("Credit to 1tsJustgp")
	local Ds1Section = Main:NewSection("Discord private gp1tsJust#3203")
	local Dserver3Section = Main:NewSection("Server Discord https://discord.gg/TWqQNcpN")


