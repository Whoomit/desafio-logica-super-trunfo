# 🃏 Desafio de Lógica: Super Trunfo

Este repositório contém o desafio de lógica de programação. O objetivo é criar um algoritmo que simule a lógica de uma rodada do jogo Super Trunfo.

## 🎯 O Desafio

Você deve criar uma função ou script que receba como entrada **duas cartas** (do Jogador 1 e do Jogador 2) e o **atributo** que o Jogador 1 escolheu para comparar.

A sua função deve ser capaz de:

1.  Comparar o valor do atributo escolhido nas duas cartas.
2.  Determinar qual jogador venceu a rodada.
3.  Lidar corretamente com as regras especiais (veja abaixo).

## 📜 Regras do Jogo

Para este desafio, vamos usar um conjunto simplificado de regras do Super Trunfo:

1.  **Comparação Simples:** O jogador que tiver o **maior** valor no atributo escolhido vence a rodada.
    * **Exceção:** Para alguns atributos (ex: "Peso" em carros), o **menor** valor pode ser o vencedor. O desafio deve especificar quais atributos seguem essa lógica invertida.

2.  **Empate:** Se os valores do atributo escolhido forem iguais, ocorre um empate. (Para este desafio, você pode apenas retornar "Empate". Em um jogo completo, as cartas iriam para um "bolo").

3.  **A Carta "Super Trunfo":** Existe uma carta especial no baralho, geralmente a "A1" ou "1A".
    * Esta carta **vence automaticamente** de todas as outras cartas (B, C, D...), **independentemente** do atributo escolhido.
    * A única exceção é se ela competir contra outra carta do grupo "A".

4.  **Regra do Grupo "A":** Se a carta "Super Trunfo" (ex: A1) competir com outra carta do grupo "A" (ex: A2, A3, A4), a regra de comparação normal (maior/menor valor) volta a valer entre elas. A carta "Super Trunfo" perde sua "magia" automática.

## 💾 Estrutura de Dados (Exemplo)

Você pode representar as cartas como objetos (ou dicionários, structs, etc., dependendo da linguagem).

**Exemplo de Tema: Carros**

* **Atributos onde "maior" vence:** `Velocidade Máxima`, `Potência`
* **Atributo onde "menor" vence:** `0-100 km/h (Tempo)`

```json
// Exemplo de como os dados das cartas podem ser
{
  "carta_jogador_1": {
    "codigo": "A1",
    "nome": "Super Máquina",
    "velocidade_max": 350,
    "potencia": 700,
    "tempo_0_100": 3.5
  },
  "carta_jogador_2": {
    "codigo": "B2",
    "nome": "Carro Comum",
    "velocidade_max": 200,
    "potencia": 150,
    "tempo_0_100": 9.0
  },
  "atributo_escolhido": "potencia"
}
```

## 📋 Requisitos da Solução

A sua solução deve ser uma função ou script (em [Linguagem, ex: Python, JavaScript, Java...]) que receba os dados e retorne o vencedor.

**Exemplo de função:**

```
funcao decidirRodada(carta1, carta2, atributo):
  // 1. Verificar se alguma carta é a "Super Trunfo" (ex: "A1")
  // 2. Verificar se ambas são do grupo "A"
  // 3. Se não for regra especial, verificar qual atributo é (se "maior" ganha ou "menor" ganha)
  // 4. Comparar os valores
  // 5. Retornar o vencedor (ex: "Jogador 1", "Jogador 2" ou "Empate")
```

## 🚀 Como Entregar

1.  Faça um **Fork** deste repositório (clicando em "Fork" no canto superior direito).
2.  Crie sua solução no seu repositório "forkado".
3.  [Defina como será a entrega. Ex: "Envie o link do seu repositório no sistema da faculdade" ou "Abra um Pull Request para este repositório."]

---
Boa sorte!
