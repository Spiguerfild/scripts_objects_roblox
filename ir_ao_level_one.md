--client 
local button = script.Parent
local event = game:GetService("ReplicatedStorage"):FindFirstChild("level_one_lobby")


button.MouseButton1Click:Connect(function()
	event:FireServer()
end)
-- ativa o evento no servidor para o script do servidor reconhecer e enviar o player local que apertou o botão.
