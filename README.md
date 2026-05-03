# Jogo de Poker — Comparador de Mãos

Projeto desenvolvido em C para a disciplina de Programação 2. O programa recebe duas mãos de poker e determina qual delas vence, aplicando as regras oficiais de classificação.

## O que o programa faz

- Lê múltiplas rodadas de entrada
- Interpreta cartas com valor (2–10, J, Q, K, A) e naipe (C, E, O, P)
- Ordena as cartas por valor e naipe para facilitar a análise
- Classifica cada mão entre as 9 combinações possíveis
- Compara as mãos e exibe a vencedora, ou `E` em caso de empate

## Combinações reconhecidas

| Combinação       | Descrição                                      |
|------------------|------------------------------------------------|
| Par              | Dois cartas de mesmo valor                     |
| Dois Pares       | Dois pares distintos                           |
| Trinca           | Três cartas de mesmo valor                     |
| Sequência        | Cinco cartas em sequência de valores           |
| Flush            | Cinco cartas do mesmo naipe                    |
| Full House       | Trinca + Par                                   |
| Quadra           | Quatro cartas de mesmo valor                   |
| Straight Flush   | Sequência do mesmo naipe                       |
| Royal Flush      | Sequência 10–A do mesmo naipe                  |

## Como compilar e executar

```bash
gcc Trabalho.c -o poker
./poker < entrada.txt
```

## Formato de entrada

```
2
A C K C Q C J C 10 C
9 P 8 P 7 P 6 P 5 P
A E A O A P K E K O
2 C 3 E 4 O 5 P 6 C
```

Primeira linha: número de rodadas  
Cada rodada: 5 cartas do jogador 1, depois 5 cartas do jogador 2  
Cada carta: valor seguido do naipe separados por espaço

## Formato de saída

A mão vencedora é exibida na ordem original das cartas. Em caso de empate: `E`

## Conceitos aplicados

- Structs e enums em C
- Algoritmo de ordenação (bubble sort)
- Lógica de verificação de combinações com contadores
- Entrada e saída formatada com `scanf` / `printf`
- Modularização com funções específicas por responsabilidade

## Autor

Heitor Monteiro Padovese  
Disciplina: Programação 2
