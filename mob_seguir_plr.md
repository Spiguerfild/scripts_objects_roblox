local distanciamax = 135 -- x metros para o NPC perSeguir o jogador
local dano_spiga = 1

local distanciamin = 6
function jogador()
	repeat wait() until game.Players.NumPlayers >= 1 -- esperar até que a quantidade de jogadores for maior que 1 ou igual
	local NPC = script.Parent
	local NPCHumanoidRoot = NPC.Part
	local NPCHumanoid = NPC.Humanoid
	for i,v in pairs(game.Players:GetPlayers()) do -- Pegar a lista dos jogadores
		repeat wait() until v.Character -- Aguardar o character do player
		if (v.Character.HumanoidRootPart.Position - NPCHumanoidRoot.Position).Magnitude <= distanciamax and (v.Character.HumanoidRootPart.Position - NPCHumanoidRoot.Position).Magnitude >= distanciamin then
			NPCHumanoid:MoveTo(v.Character.HumanoidRootPart.Position - Vector3.new(6,distanciamin,0))
		
		
				
			NPCHumanoidRoot.Touched:Connect(function(hit) -- dar dano no jogador
				

					if hit.Parent:FindFirstChild("Humanoid") then
						hit.Parent:FindFirstChild("Humanoid"):TakeDamage(dano_spiga)
dano_spiga = 0
				wait(1)
				
					dano_spiga = 1
					

					end
				end)
			end
			
		end
	end

while wait() do
	jogador()
	local npc = script.Parent
	if npc.Humanoid.Health <= 0 then
		npc:Destroy()

		local clone = 	game:GetService("ServerStorage").a_du_pneu
		clone:Clone()
		print("cloner")
		clone.Name = "A DU PNEU 2"
		clone.Humanoid.Health = 200
		clone.Parent = game:GetService("Workspace")
end

end 
