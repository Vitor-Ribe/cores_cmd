# cores_cmd
> Como colorir a saída do seu código C no CMD do Windows 🎨
#
Se você, assim como eu, gosta de deixar a saída do seu código em C mais apresentável, é bom dar uma olhada nessa dica!


Para colorir textos no console em C ou C++, você pode usar sequências de escape ANSI. Estas são sequências de caracteres especiais que, quando impressas no console, alteram a formatação do texto, incluindo sua cor.

```c
#include <stdio.h>

int main() {
    // Sequências de escape ANSI para cores
    printf("\033[0;31m"); // Define a cor vermelha
    printf("Texto vermelho\n");
    printf("\033[0;32m"); // Define a cor verde
    printf("Texto verde\n");
    printf("\033[0m");    // Restaura a cor padrão

    return 0;
}
```

Este código define a cor do texto usando sequências de escape ANSI antes de imprimir o texto e, em seguida, restaura a cor padrão após a impressão. 
#
Algumas sequências de escape ANSI que você pode testar:


- **Cores do texto:**

  - `\033[0;30m` Preto
  - `\033[0;31m` Vermelho
  - `\033[0;32m` Verde
  - `\033[0;33m` Amarelo
  - `\033[0;34m` Azul
  - `\033[0;35m` Magenta (Roxo)
  - `\033[0;36m` Ciano (Azul claro)
  - `\033[0;37m` Branco

- **Cores de fundo:**

  - `\033[0;40m` Fundo preto
  - `\033[0;41m` Fundo vermelho
  - `\033[0;42m` Fundo verde
  - `\033[0;43m` Fundo amarelo
  - `\033[0;44m` Fundo azul
  - `\033[0;45m` Fundo magenta (Roxo)
  - `\033[0;46m` Fundo ciano (Azul claro)
  - `\033[0;47m` Fundo branco
    
- **Outras opções:**
  - `\033[1m` Negrito
  - `\033[4m` Sublinhado
  - `\033[7m` Reverso (inverte a cor do texto e do fundo)
  - `\033[0m` Restaura as configurações padrão de cor e estilo
#
Você pode combinar essas sequências de escape ANSI para criar diferentes estilos de texto e fundo. Por exemplo:

```c
#include <stdio.h>

int main() {
    // Exemplos de texto colorido e estilizado
    printf("\033[0;31mTexto vermelho\033[0m\n");
    printf("\033[1;32mTexto verde em negrito\033[0m\n");
    printf("\033[4;43mTexto com sublinhado e fundo amarelo\033[0m\n");
    printf("\033[1;37;44mTexto branco em negrito com fundo azul\033[0m\n");

    return 0;
}
```
## ⚠️ Atenção!
A eficácia dessas sequências de escape depende da capacidade do console em interpretá-las corretamente.

Nem todos os consoles suportam sequências de escape ANSI. Vale a pena testar seu console antes de ir personalizando todo o código.

Além disso, em ambientes Windows, você também pode usar a biblioteca `windows.h` para colorir texto no console. No entanto, isso limita o programa a sistemas Windows.
