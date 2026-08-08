# 03 — Jogos

## Projeto 1: Pong
Jogo clássico de Pong com dois jogadores ou contra o computador.

### Sprites necessários:
- Bola
- Raquete 1 (jogador)
- Raquete 2 (computador)

### Lógica:
1. A bola se move continuamente em diagonal
2. Ao tocar nas bordas superior/inferior, inverte Y
3. Ao tocar nas raquetes, inverte X
4. Se a bola sair pela esquerda/direita, ponto para o adversário
5. Variáveis: `pontos_j1` e `pontos_j2`

---

## Projeto 2: Labirinto
O jogador controla um sprite pelo labirinto usando as setas do teclado.

### Lógica:
1. Mova o sprite com as setas (cima, baixo, esquerda, direita)
2. Se tocar na cor da parede (preto), volte à posição anterior
3. Se tocar na cor do objetivo (verde), "Você venceu!"
4. Adicione um cronômetro para desafio

---

## Projeto 3: Quiz Interativo
Quiz de perguntas e respostas com pontuação.

### Lógica:
1. Crie listas: `perguntas` e `respostas`
2. Para cada pergunta: `pergunte` e compare a `resposta`
3. Se correto: +10 pontos + efeito sonoro
4. Se errado: mostre resposta correta
5. No final: mostre pontuação total
