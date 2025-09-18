# Exercícios – Capítulo 9: Subprogramas

## Exercício 2 – Corrotinas em GoLang (primeiro contato)
As **corrotinas** permitem a execução concorrente de rotinas dentro de um programa. Em Go, isso é feito com a palavra-chave `go`.

1. Crie um arquivo chamado `main.go`.
2. Implemente o seguinte programa simples:

```go
package main

import (
    "fmt"
    "time"
)

func escrever(texto string) {
    for i := 0; i < 5; i++ {
        fmt.Println(texto, i)
        time.Sleep(time.Millisecond * 500)
    }
}

func main() {
    go escrever("Corrotina")  // executa em paralelo
    escrever("Função normal") // executa no fluxo principal
}
```

3. Compile e execute o programa com:
   ```bash
   go run main.go
   ```

**Questões:**
- O que acontece com a ordem das mensagens exibidas?
As mensagens da função normal e da corrotina aparecem intercaladas, mas a ordem exata pode variar a cada execução.

- Por que as mensagens da corrotina e da função normal se intercalam?
Porque o Go executa a função escrever("Corrotina") em paralelo, enquanto o programa continua rodando escrever("Função normal"). O escalonador da linguagem alterna entre as duas execuções.

- Relacione esse comportamento com a definição de **corrotinas** estudada no Capítulo 9.
Corrotinas permitem múltiplos pontos de execução e preservam o estado entre suspensões. Esse comportamento é visto aqui: a corrotina e a função normal compartilham o tempo de execução, e o Go controla quando cada uma avança, gerando a interlevação das mensagens.

