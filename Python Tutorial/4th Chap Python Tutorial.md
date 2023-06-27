# Capítulo 4: Funções e Módulos

## Funções

As funções são blocos de código que realizam uma tarefa específica e podem ser reutilizadas em diferentes partes de um programa. Elas ajudam a organizar o código, tornando-o mais legível, modular e fácil de manter. Em Python, você pode definir suas próprias funções utilizando a palavra-chave `def`.

### Definição e Chamada de Funções

Para definir uma função, você precisa especificar um nome para a função e os parâmetros que ela recebe (se houver), seguidos por dois pontos `:`. O corpo da função é indentado e contém as instruções que serão executadas quando a função for chamada.

```python
def saudacao():
    print("Olá! Bem-vindo(a)!")
```

Neste exemplo, a função `saudacao` é definida sem receber parâmetros. Ela simplesmente imprime uma mensagem de saudação na tela.

Para chamar uma função, você utiliza o nome da função seguido de parênteses `()`. Se a função não recebe parâmetros, os parênteses podem ser deixados vazios.

```python
saudacao()  # Chamada da função saudacao()
```

A chamada da função `saudacao()` resultará na impressão da mensagem "Olá! Bem-vindo(a)!" no console.

### Passagem de Argumentos para Funções

As funções podem receber argumentos, que são valores fornecidos quando a função é chamada. Os argumentos são utilizados dentro do corpo da função para realizar as operações desejadas. Existem diferentes formas de passar argumentos para funções em Python:

- **Argumentos posicionais**: Os argumentos são passados com base na posição em que eles são fornecidos na chamada da função. Na definição da função, os parâmetros são listados na mesma ordem em que devem ser fornecidos.

```python
def somar(a, b):
    resultado = a + b
    print(resultado)

somar(3, 4)  # Chamada da função somar() com argumentos posicionais
```

Neste exemplo, a função `somar()` recebe dois argumentos posicionais: `a` e `b`. Durante a chamada da função, são fornecidos os valores `3` e `4` para os parâmetros `a` e `b`, respectivamente. A função realiza a soma dos valores e imprime o resultado, que é `7`.

- **Argumentos com palavra-chave**: Os argumentos são passados com base em suas chaves e valores correspondentes. Durante a chamada da função, você especifica o nome do parâmetro seguido de um sinal de igual `=` e o valor correspondente.

```python
def exibir_informacoes(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)

exibir_informacoes(nome="João", idade=25)  # Chamada da função exibir_informacoes() com argumentos com palavra-chave
```

Neste exemplo, a função `exibir_informacoes()` recebe dois argumentos com palavra-chave: `nome` e `idade`. Durante a chamada da função, são fornecidos os valores `"João"` e `25` para os parâmetros `nome` e `idade`, respectivamente. A função imprime as informações na tela.

- **Argumentos padrão**: Os argumentos podem ter um valor padrão pré-definido. Caso nenhum valor seja fornecido para esses argumentos na chamada da função, o valor padrão será utilizado.

```python
def saudacao(nome="Usuário"):
    print("Olá,", nome, "!")

saudacao()  # Chamada da função saudacao() sem fornecer um argumento
saudacao("João")  # Chamada da função saudacao() fornecendo um argumento
```

Neste exemplo, a função `saudacao()` possui um parâmetro `nome` com valor padrão `"Usuário"`. Se nenhum argumento for fornecido durante a chamada da função, o valor padrão será utilizado. Caso contrário, o valor fornecido substituirá o valor padrão. As chamadas `saudacao()` e `saudacao("João")` resultarão na impressão das saudações "Olá, Usuário!" e "Olá, João!".

### Retorno de Valores em Funções

Além de executar um conjunto de instruções, as funções em Python também podem retornar valores. Isso permite que os resultados de uma função sejam utilizados em outras partes do programa. Para retornar um valor em uma função, utiliza-se a palavra-chave `return`, seguida pelo valor que será retornado.

```python
def calcular_soma(a, b):
    soma = a + b
    return soma

resultado = calcular_soma(5, 3)  # Chamada da função calcular_soma() e armazenamento do resultado retornado
print(resultado)  # Imprime o resultado (8)
```

Neste exemplo, a função `calcular_soma()` recebe dois argumentos `a` e `b`, realiza a soma e retorna o resultado. O valor retornado pela função é atribuído à variável `resultado`, que pode ser impressa ou utilizado posteriormente no programa.

O uso de retorno de valores em funções é útil quando se deseja obter um resultado específico de uma operação ou quando se deseja realizar cálculos em uma função e utilizar o resultado em outras partes do programa.

## Módulos

Módulos são arquivos Python que contêm definições de funções, classes e variáveis que podem ser reutilizadas em outros programas. Eles ajudam a organizar o código em unidades lógicas e permitem compartilhar código entre diferentes programas e projetos. Em Python, existem módulos pré-definidos que vêm com a instalação padrão da linguagem, bem como módulos personalizados que podem ser criados por você.

### Importação e Utilização de Módulos Pré-definidos

Para utilizar um módulo pré-definido, é necessário importá-lo no seu programa utilizando a palavra-chave `import`.

```python
import math

raiz_quadrada = math.sqrt(16)
print(raiz_quadrada)
```

Neste exemplo, o módulo `math` é importado para utilizar a função `sqrt()`, que calcula a raiz quadrada de um número. A função `sqrt()` é chamada para calcular a raiz quadrada de `16` e o resultado é impresso no console.

### Importação e Utilização de Módulos Personalizados

Você também pode criar seus próprios módulos personalizados para armazenar funções e outras definições. Para utilizar um módulo personalizado, basta importá-lo no seu programa da mesma forma que os módulos pré-definidos.

```python
import meu_modulo

meu_modulo.minha_funcao()
```

Neste exemplo, o módulo `meu_modulo` é importado e a função `minha_funcao()` é chamada.

Além da importação simples de um módulo completo, você pode importar partes específicas de um módulo ou atribuir um alias a um módulo para facilitar sua utilização.

```python
from meu_modulo import minha_funcao

minha_funcao()
```

Neste caso, apenas a função `minha_funcao()` é importada do módulo `meu_modulo` e pode ser chamada diretamente.

```python
import meu_modulo as mm

mm.minha_funcao()
```

Neste caso, o módulo `meu_modulo` é importado com o alias `mm`, e a função `minha_funcao()` é chamada utilizando o prefixo `mm.`.

Neste capítulo, você aprendeu sobre funções e módulos em Python. As funções permitem encapsular blocos de código para reutilização, enquanto os módulos permitem organizar e compartilhar código entre diferentes programas. Esses conceitos são fundamentais para a modularização e reutilização de código em Python, tornando seu programa mais eficiente e fácil de manter. Nos próximos capítulos, continuaremos explorando outros tópicos importantes em Python.