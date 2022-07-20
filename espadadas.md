local event = game:GetService("ReplicatedStorage").espadadas
local espada = script.Parent
local anima_one = game:GetService("ServerStorage").Katana_spig.Animation_one
local anima_two = game:GetService("ServerStorage").Katana_spig.Animation_two
local anima_three =  game:GetService("ServerStorage").Katana_spig.Animation_three

event.OnServerEvent:Connect(function()
	if (espada.Parent.One.Value == false)  then
		local humanoid = espada.Parent.Humanoid
		local track_one = humanoid:LoadAnimation(anima_one)
		track_one:Play()
		espada.Parent.One.Value = true
		
			
	elseif (espada.Parent.One.Value == true) and(espada.Parent.Two.Value == false) then
		
		local humanoid = espada.Parent.Humanoid
		local track_two = humanoid:LoadAnimation(anima_two)
		track_two:Play()
		espada.Parent.Two.Value = true
		
	elseif(espada.Parent.Two.Value == true) and(espada.Parent.Three.Value == false) then
		
		local humanoid = espada.Parent.Humanoid
		local track_three = humanoid:LoadAnimation(anima_three)
		track_three:Play()
		

		
		espada.Parent.One.Value = false --reset
		espada.Parent.Two.Value = false--reset
		espada.Parent.Three.Value = false--reset
	end
end)




local lamina = script.Parent.Lamina
local dano_ponta_espada = 0.3
lamina.Touched:Connect(function(oq_tocou)

	

	if oq_tocou.Parent:FindFirstChild("Humanoid") and oq_tocou.Parent~= lamina.Parent then 
		local humanoid = oq_tocou.Parent:FindFirstChild("Humanoid")
		humanoid.Health = humanoid.Health - dano_ponta_espada




	end


end)
