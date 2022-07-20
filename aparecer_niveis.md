--client
local frame = script.Parent.Parent
local evento = game:GetService("ReplicatedStorage"):FindFirstChild("niveis_lobby")
local buton_x = frame.Frame.button_x

evento.OnClientEvent:Connect(function()
	frame.Visible = true
end)

buton_x.MouseButton1Click:Connect(function()
	frame.Visible = false
end)

