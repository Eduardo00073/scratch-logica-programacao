# 🎮 Projeto: Jogo de Plataforma no Scratch

## Descrição
Jogo de plataforma 2D completo com:
- Física de gravidade e pulo
- Múltiplas plataformas
- Inimigos com IA simples
- Sistema de vidas e pontuação
- 3 fases progressivas

## 🔧 Mecânicas Implementadas

### 1. Física de Gravidade
```scratch
// Script do Jogador
definir [gravidade v] como (0)
definir [velocidade_y v] como (0)

sempre
  // Gravidade
  mudar [velocidade_y v] em (-1)
  mudar y em (velocidade_y)
  
  // Colisão com chão
  se <tocando em [Plataforma v]?> então
    mudar y em (2)  // empurra para cima
    definir [velocidade_y v] como (0)
    definir [no_chao v] como (1)
  senão
    definir [no_chao v] como (0)
  fim
```

### 2. Pulo
```scratch
se <tecla [espaço v] pressionada?> então
  se <(no_chao) = (1)> então
    definir [velocidade_y v] como (12)
  fim
fim
```

### 3. Inimigo Patrulheiro
```scratch
quando [bandeira verde] clicada
  sempre
    mover (3) passos
    se na borda, ricocheteie
    se <tocando em [Jogador v]?> então
      transmitir [jogador_morreu v]
    fim
  fim
```

### 4. Coletáveis (Estrelas/Moedas)
```scratch
quando [bandeira verde] clicada
  mostrar
  sempre
    se <tocando em [Jogador v]?> então
      mudar [pontos v] em (10)
      tocar som [Pop v]
      esconder
      parar [este script v]
    fim
  fim
```

## 📋 Lista de Sprites

| Sprite | Tipo | Funções |
|--------|------|---------|
| Herói | Jogador | Movimento, pulo, colisão |
| Plataforma | Cenário | Colisão, chão |
| Inimigo Cogumelo | IA | Patrulha, dano |
| Estrela | Coletável | Pontuação |
| UI | Interface | Vidas, pontos, fase |
| Gerente | Oculto | Controle de jogo |

## 🎯 Conceitos de Programação Aplicados

- **Variáveis**: vidas, pontos, fase, velocidade
- **Loops**: always loops para física e movimento
- **Condicionais**: colisões, condições de game over
- **Eventos/Mensagens**: comunicação entre sprites
- **Funções**: blocos personalizados para física
- **Vetores**: coordenadas X e Y para posição

> 📁 Para ver o projeto funcionando, acesse o link do Scratch compartilhado na pasta do repositório.
