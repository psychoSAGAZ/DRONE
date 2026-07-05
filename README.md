local player = game:GetService("Players").LocalPlayer
local gui = player:WaitForChild("PlayerGui")

local main = gui:WaitForChild("MainGUIHandler")
local buttons = main:WaitForChild("MainButtons")

-- OLD: ativar + ajustar
local old = buttons:WaitForChild("Old")

if old:IsA("GuiObject") then
	old.Visible = true
	old.Position = UDim2.new(0.200000003, 57, 0, 0)
	old.Size = UDim2.new(0.75, 0, 1, 0)
end

-- NEW: deletar
local new = buttons:FindFirstChild("New")
if new then
	new:Destroy()
end