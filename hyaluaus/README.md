# hyaluaus

Versão modificada (**hyaprojmodified**) do script de emotes de [7yd7/Hub](https://github.com/7yd7/Hub/blob/Branch/GUIS/Emotes.lua), com extras de câmera, sync de emote e keybinds.

## Como usar

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/HyaFranch/hyaluaus/refs/heads/main/Emotes.lua"))()
```

> O script carrega `GUIS/` deste repositório e as listas de emotes direto do repo original do 7yd7 (assim atualizam sozinhas). Se a sua branch não se chamar `main`,
> defina antes do loadstring:
> `getgenv().HyaRepoBase = "https://raw.githubusercontent.com/HyaFranch/hyaluaus/refs/heads/SUA_BRANCH/"`

## Estrutura

```
Emotes.lua      script principal
GUIS/           Notify, Settings (biblioteca de UI) e OpenEmote (botão mobile)
```

## Extras (aba **Extras** nas Settings)

| Recurso | O que faz |
|---|---|
| Emote Sync | copia o emote do player mais próximo (< 40 studs) |
| Camera Lock | trava a câmera numa posição fixa **do mapa** (não acompanha o boneco) |
| Cam Head | câmera segue a cabeça suavemente (ajuste de suavidade) |
| **Cam Salva 1–3** | salva a câmera **relativa ao boneco** e reaplica com um clique; acompanha o boneco quando você anda |
| Keybinds | tecla → emote (salvo em `hyaprojmodified/ExtConfig.json`) |

Camera Lock, Cam Head e Cam Salva são exclusivos: ligar um desliga os outros.

### Cam Salva — fluxo

1. Ajuste a câmera do jeito que quer (frente do boneco, de cima, de lado, distância).
2. Aba **Extras → Cam Salva N → SALVAR**.
3. Depois, **USAR** reaplica esse enquadramento; clicar de novo (**SOLTAR**) devolve a câmera ao normal.
4. Para trocar o enquadramento: **SOLTAR**, ajuste de novo e **SALVAR**.

Os slots ficam gravados no `ExtConfig.json` e continuam depois de sair e entrar de novo.

**Girar com o boneco**: `OFF` (padrão) só acompanha a posição — melhor para andar. `ON` mantém sempre a mesma face do boneco (bom parado, mas andar com a câmera na frente gira em círculos).

## Créditos

Base: [7yd7/Hub](https://github.com/7yd7/Hub) (script e GUIs originais) e listas do projeto sniper-Emote do mesmo autor.
