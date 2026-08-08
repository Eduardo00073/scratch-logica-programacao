# 04 — Animações e Histórias Interativas

## Projeto: Conto Interativo

### Objetivo
Criar uma história animada onde o espectador faz escolhas que alteram o rumo da narrativa.

### Cenários (Palcos):
1. Floresta
2. Castelo
3. Caverna

### Sprites:
- Personagem principal
- Vilão
- NPC (ajudante)

### Roteiro:
1. **Cena 1 — Floresta**: Personagem aparece e se apresenta. Pergunta ao jogador: "Ir para o Castelo ou Caverna?"
2. **Cena 2A — Castelo**: Se escolheu Castelo → encontra o vilão → luta (jogo de reflexo)
3. **Cena 2B — Caverna**: Se escolheu Caverna → encontra tesouro → puzzle
4. **Final**: Dependendo das escolhas, mostra final diferente

### Blocos importantes:
- `transmita mensagem` para trocar de cena
- `quando eu receber mensagem` para reagir
- `pergunte` para decisões do jogador
- `mude o palco para` para trocar cenários
