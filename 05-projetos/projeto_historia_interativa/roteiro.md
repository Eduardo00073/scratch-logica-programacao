# 📖 Projeto: História Interativa no Scratch

## Conceito
Uma aventura com escolhas onde o usuário decide o caminho da história.

## Estrutura de Cenas

```
Início
  └── Cena 1: Floresta
        ├── [Escolha A] → Explorar caverna
        │     ├── [A1] → Encontra tesouro → FIM BOM 🏆
        │     └── [A2] → Encontra dragão → FIM ÉPICO ⚔️
        └── [Escolha B] → Seguir rio
              ├── [B1] → Aldeia amigável → Missão de entrega
              │     └── Sucesso → FIM BOM 🏆
              └── [B2] → Terreno perigoso → FIM NEUTRO 📜
```

## Script Principal (Sprite Narrador)

```scratch
quando [bandeira verde] clicada
  // Configuração inicial
  definir [capitulo v] como (1)
  transmitir [cena_1 v]

quando receber [cena_1 v]
  mudar fundo para [floresta v]
  dizer [Você está em uma floresta misteriosa...] por (3) segundos
  dizer [O que deseja fazer?] por (2) segundos
  transmitir [mostrar_opcoes_1 v]

quando receber [escolha_A v]
  transmitir [cena_caverna v]

quando receber [escolha_B v]
  transmitir [cena_rio v]
```

## Sprites de Botão (Opções)

```scratch
// Sprite: Botão "Explorar Caverna"
quando receber [mostrar_opcoes_1 v]
  mostrar

quando este sprite for clicado
  esconder
  transmitir [escolha_A v]
```

## Conceitos Praticados

1. **Estrutura de dados**: Capítulos numerados
2. **Máquina de estados**: Cada cena é um "estado"
3. **Eventos**: Mensagens entre sprites
4. **Ramificação**: if/else como estrutura narrativa
5. **Modularidade**: Cada cena é independente

> 🎭 **Dica Criativa**: Adicione sons de ambiente, efeitos de transição entre cenas e sprites animados para deixar a história mais imersiva!
