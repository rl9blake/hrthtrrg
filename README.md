-- main.lua
local player = {
    x = 100,
    y = 300,
    width = 30,
    height = 30,
    color = {0, 1, 0}
}

local button = {
    x = 10,
    y = 10,
    width = 120,
    height = 40,
    label = "Ir para o teto"
}

local ceilingY = 50 -- "teto" do mapa

function love.load()
    love.window.setTitle("Teleporte para o Teto")
    love.window.setMode(800, 600)
end

function love.draw()
    -- Desenhar jogador
    love.graphics.setColor(player.color)
    love.graphics.rectangle("fill", player.x, player.y, player.width, player.height)

    -- Desenhar botão
    love.graphics.setColor(0.2, 0.2, 0.8)
    love.graphics.rectangle("fill", button.x, button.y, button.width, button.height)
    love.graphics.setColor(1, 1, 1)
    love.graphics.print(button.label, button.x + 10, button.y + 12)
end

function love.mousepressed(x, y, buttonCode)
    if buttonCode == 1 then -- Clique esquerdo
        if x > button.x and x < button.x + button.width and
           y > button.y and y < button.y + button.height then
            -- Teleportar jogador para o "teto"
            player.y = ceilingY
        end
    end
end
