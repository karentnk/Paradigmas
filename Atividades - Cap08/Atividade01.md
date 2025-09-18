# Atividades para Casa – Capítulo 8

## Atividade 1 – Reescrevendo código sem `goto`
Você recebeu o seguinte pseudocódigo, escrito de forma semelhante ao estilo das primeiras versões do Fortran, utilizando `goto`:

```text
i := 1
goto check

loop:
    print(i)
    i := i + 1

check:
    if (i <= 10) then
        goto loop
```

**Tarefas:**
1. Reescreva o código acima utilizando um laço de repetição pré-teste (`while`) em uma linguagem de sua escolha (C, Java, Python, etc.).

```c
#include <stdio.h>

int main() {
    int i = 1;
    while (i <= 10) {
        printf("%d\n", i);
        i = i + 1;
    }
    return 0;
}
```

2. Reescreva novamente utilizando um laço de repetição controlado por contador (`for`).
3. 
```c
#include <stdio.h>

int main() {
    for (int i = 1; i <= 10; i++) {
        printf("%d\n", i);
    }
    return 0;
}
```
3. Compare os três códigos (original com `goto`, versão com `while` e versão com `for`) e escreva um pequeno parágrafo discutindo qual forma é mais legível e por quê.

- **Resposta:** O código com goto funciona, mas é confuso porque a gente precisa ficar acompanhando os saltos. O while já mostra melhor que a repetição acontece enquanto a condição for verdadeira. O for é o mais simples nesse caso, porque mostra de cara onde a variável começa, até onde vai e como aumenta. Por isso, o for é o mais fácil de entender e ler.
---
