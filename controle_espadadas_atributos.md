local ws = game:GetService("Workspace")
local character = script.Parent

local classe_escolha = Instance.new("BoolValue")
classe_escolha.Parent = character --pai
classe_escolha.Name = "One" --nome

local classe_escolha = Instance.new("BoolValue")
classe_escolha.Parent = character --pai
classe_escolha.Name = "Two" --nome

local classe_escolha = Instance.new("BoolValue")
classe_escolha.Parent = character --pai
classe_escolha.Name = "Three" --nome
-- este sistema controla as espadadas do player, foram criadas 3 animações quando uma é completada o valor boolean do player de nome one fica true
--depois a programação executa outra animação e deixa o segundo(Two) true 
--e por fim ele executa a 3° espadada e reseta todos os boolean do player
