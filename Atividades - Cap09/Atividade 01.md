# Exercícios – Capítulo 9: Subprogramas

## Exercício 1 – Passagem de Parâmetros por Valor e por Referência
Considere o seguinte pseudocódigo de uma função que tenta dobrar o valor de um número:

```text
procedure dobrar(x)
    x := x * 2
end
```
1. Implemente esse subprograma em **C** duas vezes:
   - A primeira versão recebendo o parâmetro **por valor**.
   - A segunda versão recebendo o parâmetro **por referência** (usando ponteiros).

//Por valor
#include <stdio.h>

void dobrarValor(int x) {
    x = x * 2;
    printf("Por valor: %d\n", x);
}

//Por referência
#include <stdio.h>

void dobrarReferencia(int *x) {
    *x = *x * 2;
    printf("Por referencia: %d\n", *x);
}


2. Escreva um programa principal que:
   - Crie uma variável inteira com valor inicial 10.
   - Chame a função `dobrar` por valor e exiba o resultado.
   - Chame a função `dobrar` por referência e exiba o resultado.

#include <stdio.h>

void dobrarValor(int x) {
    x = x * 2;
    printf("por valor: %d\n", x);
}
void dobrarReferencia(int *x) {
    *x = *x * 2;
    printf("por referencia: %d\n", *x);
}
int main() {
    int numero = 10;

    printf("Valor: %d\n", numero);

    dobrarValor(numero);
    printf("Por valor: %d\n", numero);

    dobrarReferencia(&numero);
    printf("Por referencia: %d\n", numero);
    return 0;
}
Saída:
Valor: 10
Por valor: 20
Por valor: 10
Por referencia: 20
Por referencia: 20


**Questões:**
- Qual a diferença observada entre as duas versões?
Na chamada por valor, a variável original não muda, só a cópia interna da função.
Na chamada por referência, a variável original é alterada.

- Por que o valor da variável só se altera na versão por referência?
Porque na passagem por valor a função recebe apenas uma cópia. Já na referência, a função recebe o endereço de memória e altera diretamente a variável original.

- Relacione essa diferença com as estratégias de passagem de parâmetros discutidas no Capítulo 9.
A passagem por valor é mais segura e evita efeitos colaterais, mas não permite alterar o argumento original. Já a passagem por referência é eficiente e permite modificar a variável fora da função, mas pode gerar efeitos colaterais indesejados. Esse exercício mostra exatamente essa diferença prática.
---

