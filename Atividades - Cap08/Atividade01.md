# Atividades para Casa – Capítulo 8

## Atividade 1 – Reescrevendo código sem `goto`

**Tarefas:**
1. Reescreva o código acima utilizando um laço de repetição pré-teste (`while`) em uma linguagem de sua escolha (C, Java, Python, etc.).
//em C
#include <stdio.h>

int main() {
    int i = 1;
    while (i <= 10) {
        printf("%d\n", i);
        i = i + 1;
    }
    return 0;
}

2. Reescreva novamente utilizando um laço de repetição controlado por contador (`for`).
//em C
#include <stdio.h>

int main() {
    for (int i = 1; i <= 10; i++) {
        printf("%d\n", i);
    }
    return 0;
}

3. Compare os três códigos (original com `goto`, versão com `while` e versão com `for`) e escreva um pequeno parágrafo discutindo qual forma é mais legível e por quê.

O código com goto funciona, mas é confuso porque a gente precisa ficar acompanhando os saltos. O while já mostra melhor que a repetição acontece enquanto a condição for verdadeira. O for é o mais simples nesse caso, porque mostra de cara onde a variável começa, até onde vai e como aumenta. Por isso, o for é o mais fácil de entender e ler.
---

## Atividade 2 – Seleção múltipla em diferentes linguagens
Muitos programas oferecem menus interativos. Suponha que você precisa implementar um menu com as seguintes opções:

1. Calcular o quadrado de um número.
2. Calcular o fatorial de um número.
3. Sair do programa.

**Tarefas:**
1. Implemente esse menu em **C** utilizando `switch/case`.
2. Implemente o mesmo menu em **Python**, utilizando apenas `if/elif/else`.
3. Execute os dois programas e compare as soluções em relação à clareza e quantidade de código.
4. Escreva um comentário final destacando em qual linguagem foi mais simples de implementar e justificar o motivo.

---

## Atividade 3 – Explorando alternativas ao `goto`
Historicamente, o `goto` foi usado para resolver diferentes tipos de desvio. Hoje, a maioria das linguagens fornece alternativas como `break`, `continue` e `return`.

**Tarefas:**
1. Escreva um programa que percorra uma lista de números inteiros e:
   - Pare imediatamente a execução ao encontrar o número 0 (`break`).
   - Pule os números negativos sem processá-los (`continue`).
   - Retorne o dobro do primeiro número par encontrado (`return`).
2. Comente sobre como seria a implementação desse mesmo programa utilizando apenas `goto` e rótulos, destacando as vantagens da abordagem moderna.
