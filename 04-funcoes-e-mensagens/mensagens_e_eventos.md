# 📨 Mensagens e Eventos no Scratch

## O que são Mensagens?

Mensagens permitem que **sprites se comuniquem** entre si.
É como o padrão **Observer/EventBus** da programação orientada a eventos!

## Transmitir e Receber

### Transmitir uma mensagem:
```scratch
transmitir [inicio v]
// ou aguardar todos receberem:
transmitir [inicio v] e esperar
```

### Receber uma mensagem:
```scratch
quando receber [inicio v]
  dizer [Recebi o sinal!] por (1) segundos
```

## 🎮 Exemplo: Jogo Multi-Sprite

### Sprite Gerente (controla o jogo):
```scratch
quando [bandeira verde] clicada
  definir [fase v] como (1)
  transmitir [iniciar_fase v]

quando receber [fase_completa v]
  mudar [fase v] em (1)
  se <(fase) > (3)> então
    transmitir [fim_de_jogo v]
  senão
    transmitir [iniciar_fase v]
  fim
```

### Sprite Inimigo:
```scratch
quando receber [iniciar_fase v]
  mostrar
  definir [velocidade v] como ((fase) * (2))
  sempre
    mover (velocidade) passos
    se na borda, ricocheteie
    se <tocando em [Jogador v]?> então
      transmitir [jogador_morreu v]
    fim
  fim
```

## Blocos Personalizados (Funções!)

### Criar um Bloco:
1. Vá em **"Mais Blocos"**
2. Clique em **"Criar um bloco"**
3. Dê um nome e adicione parâmetros

```scratch
// Definição:
definir mover_sprite (direcao) (velocidade)
  apontar em direção (direcao) graus
  mover (velocidade) passos

// Uso:
quando [bandeira verde] clicada
  sempre
    se <tecla [w v] pressionada?> então
      mover_sprite (90) (5)
    fim
  fim
```

## Conexão com Programação Real

| Scratch | JavaScript | Python |
|---------|------------|--------|
| `transmitir [evento]` | `emit('evento')` | `pubsub.publish('evento')` |
| `quando receber [evento]` | `on('evento', fn)` | `pubsub.subscribe('evento', fn)` |
| `Blocos personalizados` | `function nome() {}` | `def nome():` |
| `Variáveis locais` | `let x = 0` | `x = 0` |
| `Variáveis globais` | `window.x` | `global x` |

> 💡 **Insight**: Quando você aprende Scratch, está aprendendo a mesma lógica de JavaScript com eventos e React com props!
