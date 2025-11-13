local Games = {
    [85211729168715] = { -- Blox Fruit Sea 1
        gui = "https://raw.githubusercontent.com/bac1916r30-a11y/Farm-aura/refs/heads/main/Gui%20Farm%20Aura",
        teleport = "https://raw.githubusercontent.com/bac1916r30-a11y/Farm-aura/refs/heads/main/Teleport%20Sea1"
    },
    [79091703265657] = { -- Blox Fruit Sea 2
        gui = "https://raw.githubusercontent.com/bac1916r30-a11y/Farm-aura/refs/heads/main/Gui%20Farm%20Aura",
        teleport = "https://raw.githubusercontent.com/bac1916r30-a11y/Farm-aura/refs/heads/main/Teleport%20Sea2"
    },
    [100117331123089] = { -- Blox Fruit Sea 3
        gui = "https://raw.githubusercontent.com/bac1916r30-a11y/Farm-aura/refs/heads/main/Gui%20Farm%20Aura",
        teleport = "https://raw.githubusercontent.com/bac1916r30-a11y/Farm-aura/refs/heads/main/Teleport%20Sea3"
    }
}

local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local PlaceId = game.PlaceId

if Games[PlaceId] then
    -- Load GUI trước
    if Games[PlaceId].gui then
        pcall(function()
            loadstring(game:HttpGet(Games[PlaceId].gui))()
        end)
    end
    -- Đợi 2 giây trước khi load teleport
    wait(2)
    -- Load teleport
    if Games[PlaceId].teleport then
        pcall(function()
            loadstring(game:HttpGet(Games[PlaceId].teleport))()
        end)
    end
end
