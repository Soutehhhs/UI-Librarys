- Crie uma Part chamada "BolaMovel" no Workspace
local bolaMovel = Instance.new("Part")
bolaMovel.Name = "BolaMovel"
bolaMovel.Size = Vector3.new(5, 5, 5)
bolaMovel.BrickColor = BrickColor.Gray() -- Defina a cor cinza
bolaMovel.Anchored = true
bolaMovel.Position = Vector3.new(0, 10, 0) -- Posição inicial

-- Adicione um ClickDetector à bola
local clickDetector = bolaMovel:FindFirstChild("ClickDetector")
if not clickDetector then
    clickDetector = Instance.new("ClickDetector")
    clickDetector.Parent = bolaMovel
end

-- Função para alternar a visão através das paredes
local verAtravesDasParedes = false
local function alternarVisao()
    verAtravesDasParedes = not verAtravesDasParedes
    if verAtravesDasParedes then
        -- Ative a visão através das paredes (coloque seu código aqui)
        print("Visão ativada!")
    else
        -- Desative a visão através das paredes (coloque seu código aqui)
        print("Visão desativada!")
    end
end

-- Quando a bola for clicada, chame a função de alternar visão
clickDetector.MouseClick:Connect(alternarVisao)

-- Adicione um botão "X" para minimizar a bola
local xButton = Instance.new("TextButton")
xButton.Name = "XButton"
xButton.Text = "X"
xButton.Size = UDim2.new(0, 30, 0, 30)
xButton.Position = UDim2.new(1, -30, 0, 0)
xButton.Parent = bolaMovel

-- Quando o botão "X" for clicado, esconda a bola
xButton.MouseButton1Click:Connect(function()
    bolaMovel:Destroy()
end)
