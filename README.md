# Documentação do Projeto: Calculadora Orange

## Descrição do Projeto

O projeto **Orange Calculator** é uma calculadora gráfica com uma interface simples e intuitiva, construída com o framework **PySide6** (Qt para Python). Ela oferece funcionalidades básicas de cálculo e operações matemáticas avançadas, como funções trigonométricas e radicais. O projeto permite que o usuário alterne entre a visualização de uma área de memória para armazenar operações anteriores e realizar cálculos em tempo real.

### Funcionalidades Principais

1. **Operações Básicas**: Soma, subtração, multiplicação e divisão.
2. **Funções Trigonométricas**: Cálculos envolvendo funções seno, cosseno e tangente, com suporte para graus.
3. **Raiz Quadrada**: Cálculo da raiz quadrada com o símbolo "√".
4. **Visibilidade da Memória**: Exibição de operações anteriores realizadas.
5. **Limpeza e Backspace**: Funções para apagar o último caractere ou limpar toda a tela.
6. **Cálculos com Parênteses**: Suporte para expressões que utilizam parênteses para controle de precedência de operações.

---

## Arquitetura do Código

### 1. Estrutura de Diretórios
    Foram criados em um Framework ao qual estou desenvolvendo para criar projetos simples com **PySide6**


### 2. Classes e Métodos

#### **Classe: Calculator**

Esta é a classe principal do projeto que estende `QMainWindow` do PySide6. Ela contém os seguintes componentes e métodos:

- **`__init__(self)`**: Inicializa a calculadora, definindo o layout da interface, o ícone da janela, e criando os botões para as operações.

- **`create_buttons(self)`**: Cria os botões da calculadora, associando os botões a suas respectivas operações, e define o estilo de cada botão (operadores, funções trigonométricas, parênteses, etc.).

- **`toggle_memory_visibility(self)`**: Permite alternar a visibilidade da área de memória, onde são armazenadas e exibidas as operações anteriores.

- **`on_button_click(self)`**: Define o comportamento de cada botão quando clicado. Ele lida com a adição de números e operadores na tela, assim como com a execução de operações como "=" (igual), "C" (limpar) e "←" (backspace).

- **`on_equal_click(self)`**: Realiza o cálculo da expressão matemática digitada, substituindo os símbolos como "√" para a operação de raiz quadrada e as funções trigonométricas para suas formas matemáticas equivalentes. Caso haja erro na expressão, ele exibe um exemplo de operação válida.

- **`on_backspace(self)`**: Apaga o último caractere da expressão na tela de resultados.

- **`expression_replace(self, expression)`**: Limpa a expressão substituindo símbolos específicos para exibição de uma forma mais amigável e compreensível (por exemplo, removendo a palavra "math." de expressões matemáticas).

---

## Funções Matemáticas

### Funções Básicas

- **Soma (`+`)**
- **Subtração (`-`)**
- **Multiplicação (`*`)**
- **Divisão (`/`)**
- **Raiz Quadrada (`√`)**: Substituída internamente por `math.sqrt()`.

### Funções Trigonométricas

- **Seno (`sin`)**: Calculado em graus e convertido para radianos internamente.
- **Cosseno (`cos`)**: Calculado em graus e convertido para radianos internamente.
- **Tangente (`tan`)**: Calculado em graus e convertido para radianos internamente.

### Operações com Parênteses
Ainda estou trabalhando nisso !
A calculadora suporta o uso de parênteses para definir a ordem de operações, permitindo expressões como `(2 + 3) * 5`.

---

## Exemplo de Uso

1. **Abrindo a Calculadora**
   - Ao iniciar a aplicação, a janela da calculadora será exibida. O layout inclui a tela de memória, a tela de resultados e os botões de operações.

2. **Realizando Cálculos**
   - Digite uma expressão, como `5 + 3`, e clique no botão `=` para ver o resultado.
   - Para calcular a raiz quadrada de um número, utilize o botão "√" e insira, por exemplo, `√25`.

3. **Funções Trigonométricas**
   - Para calcular o seno de um ângulo, insira `sin(30)` e clique em `=`.
   - O mesmo vale para o cosseno e tangente, usando os botões correspondentes.

4. **Memória**
   - Após realizar uma operação, o resultado e a operação são armazenados na área de memória. O usuário pode visualizar as operações anteriores.

---

## Tratamento de Erros

Se o usuário inserir uma expressão inválida, como uma operação impossível, o código captura o erro e exibe uma mensagem amigável com exemplos válidos de operações. Por exemplo, se o usuário digitar uma expressão inválida, a calculadora pode sugerir um exemplo como:

Erro. Exemplo válido: √25

Esse tratamento de erro é útil para guiar o usuário a inserir as expressões corretamente.

---
## Link de Download

Você pode baixar a versão mais recente da **Orange Calculator** clicando no link abaixo:

[Download Orange Calculator v1.0](https://github.com/eusouanderson/orange_calculator/releases)

## Screenshot

![Captura de Tela](https://github.com/eusouanderson/orange_calculator/blob/main/screenshot.png)
