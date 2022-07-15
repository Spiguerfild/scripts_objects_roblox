--client
local player = game:GetService("Players").LocalPlayer
local mouse = player:GetMouse()
local event = game:GetService("ReplicatedStorage").espadadas


mouse.Button1Down:Connect(function()
		event:FireServer()
	event = nil
	wait(0.5)-- antimissclick
	event = game:GetService("ReplicatedStorage").espadadas
	end)
