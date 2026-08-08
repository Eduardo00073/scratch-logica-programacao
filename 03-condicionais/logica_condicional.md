# 🔀 Condicionais no Scratch — Tomada de Decisões

## O que são Condicionais?

Condicionais permitem que o programa **tome decisões** baseado em condições.

```
SE (condição é verdadeira)
  ENTÃO → executar ação A
SENÃO
  → executar ação B
FIM
```

## Tipos de Blocos Condicionais

### 1. Se...então
```scratch
se <tocando em [Parede v]?> então
  mudar cor por (25)
  tocar som [Boing v]
fim
```

### 2. Se...então...senão
```scratch
se <(pontos) > (100)> então
  dizer [Você ganhou!] por (2) segundos
  parar [tudo v]
senão
  dizer [Continue tentando!] por (1) segundos
fim
```

### 3. Condicionais Aninhadas
```scratch
se <(nota) >= (90)> então
  dizer [A — Excelente!]
senão
  se <(nota) >= (70)> então
    dizer [B — Bom!]
  senão
    se <(nota) >= (50)> então
      dizer [C — Regular]
    senão
      dizer [F — Reprovado]
    fim
  fim
fim
```

## 🎮 Projeto: Jogo de Pegada

```scratch
// Sprite: Jogador (seta)
quando [bandeira verde] clicada
  ir para x:(0) y:(-150)
  definir [pontos v] como (0)
  definir [vidas v] como (3)
  sempre
    se <tecla [seta à esquerda v] pressionada?> então
      mover (-5) passos
    fim
    se <tecla [seta à direita v] pressionada?> então
      mover (5) passos
    fim
    se <tocando em [Inimigo v]?> então
      mudar [vidas v] em (-1)
      ir para x:(0) y:(-150)
      se <(vidas) = (0)> então
        dizer [Game Over!] por (2) segundos
        parar [tudo v]
      fim
    fim
  fim
```

## Operadores Lógicos no Scratch

| Bloco | Significado | Exemplo |
|-------|-------------|---------|
| `<> e <>` | AND — ambos verdadeiros | tecla E tocando inimigo |
| `<> ou <>` | OR — um deles verdadeiro | tecla A ou tecla esquerda |
| `não <>` | NOT — inverte | não tocando parede |

## 🏆 Desafios

1. **Calculadora**: Compare dois números e diga qual é maior
2. **Quiz**: 5 perguntas com pontuação
3. **RPG Simples**: Escolhas que levam a histórias diferentes
