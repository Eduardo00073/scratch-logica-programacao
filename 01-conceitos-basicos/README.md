# 📌 01 — Conceitos Básicos do Scratch

Este módulo cobre os fundamentos do Scratch para iniciantes absolutos.

## 🎯 Objetivos de Aprendizagem

Ao final deste módulo, o aluno será capaz de:
- Navegar pela interface do Scratch (Sprites, Palco, Blocos, Scripts)
- Criar animações simples com personagens
- Entender o conceito de **evento → ação**
- Usar blocos de movimento, aparência e som

## 📚 Projetos Deste Módulo

| Projeto | Dificuldade | Conceitos |
|---------|-------------|-----------|
| Olá Mundo | ⭐ | Eventos, balões de fala |
| Gato Dançarino | ⭐ | Movimento, troca de fantasia |
| Instrumento Musical | ⭐⭐ | Teclado, sons |
| Contador Simples | ⭐⭐ | Variáveis, operadores |

## 🖥️ Interface do Scratch

```
┌──────────────────────────────────────────────┐
│  Paleta de Blocos  │    Área de Scripts       │
│  ─────────────────  │  ─────────────────────   │
│  Movimento         │  quando bandeira clicada  │
│  Aparência         │  ┌──────────────────┐     │
│  Som               │  │ mover 10 passos  │     │
│  Eventos           │  └──────────────────┘     │
│  Controle          │  ┌──────────────────┐     │
│  Sensores          │  │ próxima fantasia  │     │
│  Operadores        │  └──────────────────┘     │
│  Variáveis         │                           │
├──────────────────────────────────────────────┤
│          PALCO (480x360)                      │
│    Sprites: personagens e objetos             │
└──────────────────────────────────────────────┘
```

## 🎮 Projeto 1: Olá Mundo

### Blocos necessários:
```scratch
quando [bandeira verde] clicada
dizer [Olá! Eu sou o Gato do Scratch!] por (2) segundos
mudar efeito [cor] em (25)
tocar som [Miau v]
```

### Passo a Passo:
1. Abra o Scratch em https://scratch.mit.edu
2. Clique na aba "Scripts"
3. Arraste o bloco **"quando bandeira verde clicada"** para a área de scripts
4. Conecte o bloco **"dizer [] por [] segundos"**
5. Digite sua mensagem e pressione ▶️

## 🎮 Projeto 2: Gato Dançarino

### Blocos necessários:
```scratch
quando [bandeira verde] clicada
sempre
  mover (10) passos
  próxima fantasia
  esperar (0.2) segundos
  se na borda, ricocheteie
```

## 🏆 Desafio do Módulo

Crie um projeto que:
1. Tenha pelo menos **2 sprites**
2. Use **3 tipos diferentes de blocos**
3. Inclua uma **variável** para contar algo
4. Tenha **sons** ou **músicas**

> 💡 **Dica**: Compartilhe seu projeto e copie o link para entregar!
