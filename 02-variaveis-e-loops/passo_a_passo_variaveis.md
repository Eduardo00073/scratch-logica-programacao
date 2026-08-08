# 📊 Variáveis e Loops no Scratch

## O que são Variáveis?

Uma variável é como uma **caixinha** que guarda um valor que pode mudar.

### Criando uma Variável no Scratch
1. Clique na categoria **"Variáveis"** (laranja)
2. Clique em **"Criar uma Variável"**
3. Dê um nome: **pontos**, **vidas**, **velocidade**
4. Marque se é "Para todos os sprites" ou "Somente para este sprite"

## 🔁 Tipos de Loops

### 1. Sempre (Loop Infinito)
```scratch
sempre
  mover (5) passos
  esperar (0.1) segundos
```
→ Executa para sempre. Use para animações contínuas.

### 2. Repetir N vezes
```scratch
repetir (10) vezes
  mover (15) passos
  esperar (0.05) segundos
```
→ Executa exatamente N vezes, depois continua.

### 3. Repetir até que...
```scratch
repetir até que <(vidas) = (0)>
  esperar (0.1) segundos
```
→ Executa até a condição ser verdadeira.

## 🎮 Projeto: Contador de Cliques

```scratch
quando [bandeira verde] clicada
  definir [cliques v] como (0)

quando este sprite for clicado
  mudar [cliques v] em (1)
  dizer (juntar [Cliques: ] (cliques)) por (1) segundos
  se <(cliques) = (10)> então
    dizer [Parabéns! 10 cliques!] por (2) segundos
  fim
```

## 🎮 Projeto: Tabuada Animada

```scratch
quando [bandeira verde] clicada
  perguntar [Qual tabuada? (1-10)] e esperar
  definir [numero v] como (resposta)
  definir [i v] como (1)
  repetir (10) vezes
    dizer (juntar (juntar (numero) [x]) (juntar (i) (juntar [=] ((numero)*(i))))) por (1) segundos
    mudar [i v] em (1)
  fim
```

## 🏆 Desafios

1. **Cronômetro**: Use variáveis para contar segundos
2. **Jogo de Adivinhação**: Número secreto + tentativas
3. **Calculadora**: Somar, subtrair, multiplicar

> 💡 **Conceito de Programação**: Variáveis no Scratch são exatamente como variáveis em JavaScript, Python, Java. A lógica é idêntica!
