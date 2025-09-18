# Atividades para Casa – Capítulo 8

## Atividade 2 – Seleção múltipla em diferentes linguagens
Muitos programas oferecem menus interativos. Suponha que você precisa implementar um menu com as seguintes opções:

1. Calcular o quadrado de um número.
2. Calcular o fatorial de um número.
3. Sair do programa.

**Tarefas:**
1. Implemente esse menu em **C** utilizando `switch/case`.
```c
#include <stdio.h>
int fatorial(int n) {
    int fat = 1;
    for (int i = 1; i <= n; i++) {
        fat *= i;
    }
    return fat;
}
int main() {
    int opcao, num;

    do {
        printf("Menu:");
        printf("1. Calcular quadrado");
        printf("2. Calcular fatorial");
        printf("3. Sair");
        printf("Escolha uma opcao: ");
        scanf("%d", &opcao);

        switch (opcao) {
            case 1:
                printf("Digite um num: ");
                scanf("%d", &num);
                printf("Quadrado: %d\n", num * num);
                break;
            case 2:
                printf("Digite um num: ");
                scanf("%d", &num);
                printf("Fatorial: %d\n", fatorial(num));
                break;
            case 3:
                printf("Sai");
                break;
            default:
                printf("Opcao invalida");
        }
    } while (opcao != 3);
    return 0;
}
```
2. Implemente o mesmo menu em **Python**, utilizando apenas `if/elif/else`.
```c
def fatorial(n):
    fat = 1
    for i in range(1, n + 1):
        fat *= i
    return fat
while True:
    print("Menu:")
    print("1. Calcular o quadrado")
    print("2. Calcular o fatorial")
    print("3. Sair")

    opcao = int(input("Escolha: "))

    if opcao == 1:
        num = int(input("Digite um num: "))
        print("Quadrado:", num * num)
    elif opcao == 2:
        num = int(input("Digite um num: "))
        print("Fatorial:", fatorial(num))
    elif opcao == 3:
        print("Saindo...")
        break
    else:
        print("Opcao invalida")
```
3. Execute os dois programas e compare as soluções em relação à clareza e quantidade de código.

- **Resposta:** No programa em C, usando switch/case, o código ficou maior porque foi necessário declarar variáveis com tipos, criar uma função para o fatorial e usar scanf e printf para interação. Já no Python, usando apenas if/elif/else, a implementação ficou mais curta e fácil de entender, pois não precisamos declarar tipos e a sintaxe é mais simples. Assim, o código em Python acaba sendo mais claro e direto do que o equivalente em C.

4. Escreva um comentário final destacando em qual linguagem foi mais simples de implementar e justificar o motivo.

- **Resposta:** A versão em Python foi mais simples de implementar porque a linguagem é mais enxuta, não exige declarar tipos e a leitura do código é mais clara. Já em C o programa funciona bem, mas exige mais linhas de código e mais detalhes de implementação.

---

