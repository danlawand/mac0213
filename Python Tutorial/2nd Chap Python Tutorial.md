# Capítulo 2: Sintaxe Básica

Neste capítulo, vamos explorar a sintaxe básica da linguagem Python. Veremos a estrutura de um programa Python, os diferentes tipos de dados e operadores disponíveis, bem como as estruturas de controle de fluxo.

## 2.1 Estrutura de um Programa Python

Um programa Python é composto por instruções escritas em linhas sequenciais. Cada instrução é executada uma após a outra, a menos que haja estruturas de controle de fluxo que alterem o fluxo normal de execução. Um programa Python é geralmente iniciado com a definição de funções e/ou a execução do código diretamente.

```python
# Exemplo de estrutura de um programa Python

# Definição de uma função
def saudacao():
    print("Olá, seja bem-vindo!")

# Chamada da função
saudacao()

# Execução de código diretamente
print("Este é um programa em Python.")
```

Neste exemplo, temos a definição da função `saudacao()`, que imprime uma mensagem de saudação. Em seguida, chamamos essa função para executar o código contido nela. Além disso, temos uma instrução que imprime uma mensagem diretamente.

## 2.2 Variáveis e Tipos de Dados

Em Python, as variáveis são usadas para armazenar valores. Uma variável é criada atribuindo um valor a ela. Python é uma linguagem de tipagem dinâmica, o que significa que você não precisa especificar explicitamente o tipo de uma variável. Os tipos de dados básicos em Python incluem:

### Números

- **Inteiros (`int`)**: Números inteiros, como `42` ou `-10`.
- **Números de ponto flutuante (`float`)**: Números com casas decimais, como `3.14` ou `-2.5`.
- **Números complexos (`complex`)**: Números com uma parte real e uma parte imaginária, como `1+2j` ou `-3+4j`.

```python
# Exemplos de números em Python
idade = 25
peso = 68.5
altura = 1.75

# Exemplo de operações aritméticas
soma = idade + peso
resultado = altura * 2 - soma
```

### Strings

- **Strings**: Sequências de caracteres, delimitadas por aspas simples (`'`) ou aspas duplas (`"`).

```python
# Exemplos de strings em Python
nome = "João"
sobrenome = 'Silva'

# Concatenação de strings
nome_completo = nome + " " + sobrenome

# Acesso a caracteres individuais
primeira_letra = nome[0]
```

### Booleanos

- **Booleanos**: Valores `True` (verdadeiro) ou `False` (falso) que representam a lógica booleana.

```python
# Exemplos de booleanos em Python
temperatura = 28
chovendo = False

# Exemplo de operações lógicas
if temperatura > 25 and not chovendo:
    print("Está quente e não está chovendo.")
else:
    print("O clima não está

 tão agradável.")
```

## 2.3 Operadores Aritméticos, Lógicos e de Comparação

Python suporta uma variedade de operadores para realizar operações aritméticas, lógicas e de comparação. Alguns dos operadores comuns incluem:

- **Operadores Aritméticos**: `+` (adição), `-` (subtração), `*` (multiplicação), `/` (divisão), `%` (módulo), `**` (potência).

```python
# Exemplos de operadores aritméticos
soma = 10 + 5
subtracao = 20 - 7
multiplicacao = 4 * 6
divisao = 15 / 3
resto = 17 % 4
potencia = 2 ** 3
```

- **Operadores Lógicos**: `and` (e), `or` (ou), `not` (não).

```python
# Exemplos de operadores lógicos
temperatura = 28
chovendo = False

if temperatura > 25 and not chovendo:
    print("Está quente e não está chovendo.")

if temperatura < 20 or chovendo:
    print("Está frio ou está chovendo.")
```

- **Operadores de Comparação**: `==` (igual a), `!=` (diferente de), `>` (maior que), `<` (menor que), `>=` (maior ou igual a), `<=` (menor ou igual a).

```python
# Exemplos de operadores de comparação
idade = 18

if idade == 18:
    print("Você completou 18 anos.")

if idade < 21:
    print("Você é menor de idade.")

if idade >= 65:
    print("Você é um idoso.")
```

## 2.4 Estruturas de Controle de Fluxo

Python oferece estruturas de controle de fluxo que permitem alterar o fluxo de execução do programa. As principais estruturas de controle de fluxo incluem:

### Condicional `if/else`

A estrutura condicional `if/else` permite executar um bloco de código se uma condição for verdadeira e outro bloco de código se a condição for falsa.

```python
# Exemplo de condicional if/else
idade = 18

if idade >= 18:
    print("Você pode dirigir.")
else:
    print("Você não pode dirigir.")
```

No exemplo acima, a condição `idade >= 18` é avaliada. Se for verdadeira, o bloco de código dentro do `if` é executado e imprime "Você pode dirigir.". Caso contrário, o bloco de código dentro do `else` é executado e imprime "Você não pode dirigir.".

Há a opção de se ter múltiplos condicionais consecutivos, dessa forma se utilizaria o `elif`. 

O `elif` é uma construção que permite adicionar uma condição adicional em uma estrutura condicional `if/else`. O `elif` é uma abreviação de "else if", indicando que a condição está sendo verificada como uma alternativa ao `if` anterior.

A estrutura geral de uma construção `if/elif/else` é a seguinte:

```python
if condição1:
    # bloco de código executado se condição1 for verdadeira
elif condição2:
    # bloco de código executado se condição2 for verdadeira
elif condição3:
    # bloco de código executado se condição3 for verdadeira
else:
    # bloco de código executado se nenhuma das condições anteriores for verdadeira
```

O `elif` é usado quando há mais de duas opções possíveis e é necessário verificar uma condição adicional se a primeira condição (`if`) não for verdadeira. Cada `elif` pode ter sua própria condição para verificar.

Veja um exemplo prático que verifica a faixa etária e imprime uma mensagem correspondente:

```python
idade = 25

if idade < 18:
    print("Você é menor de idade.")
elif idade >= 18 and idade < 65:
    print("Você é adulto.")
else:
    print("Você é um idoso.")
```

Nesse exemplo, a condição `idade < 18` é verificada primeiro. Se for verdadeira, imprime-se "Você é menor de idade". Caso contrário, a próxima condição `idade >= 18 and idade < 65` é verificada. Se essa condição for verdadeira, imprime-se "Você é adulto". Se nenhuma das condições anteriores for verdadeira, o bloco de código no `else` é executado e imprime-se "Você é um idoso".

O uso do `elif` evita a necessidade de encadear vários blocos `if` um após o outro, tornando o código mais conciso e legível. É importante observar que apenas o bloco de código correspondente à primeira condição verdadeira será executado. Os blocos de código subsequentes não serão executados mesmo que suas condições sejam verdadeiras.


### Loops `for`

A estrutura de loop `for` permite iterar sobre uma sequência (como uma lista) ou um intervalo específico de valores.

```python
# Exemplo de loop for
frutas = ["maçã", "banana", "laranja"]

for fruta in frutas:
    print(fruta)
```

Neste exemplo, a lista `frutas` contém três elementos. O loop `for` itera sobre cada elemento da lista, atribuindo-o à variável `fruta`. A cada iteração, o bloco de código dentro do loop é executado, imprimindo o valor da variável `fruta`. O resultado será a impressão de cada fruta em uma linha separada.

### Loops `while`

A estrutura de loop `while` executa um bloco de código repetidamente enquanto uma condição especificada for verdadeira.

```python
# Exemplo de loop while
contador = 0

while contador < 5:
    print(contador)
    contador += 1
```

Neste exemplo, a variável `contador` é inicializada com o valor 0. O bloco de código dentro do loop é executado enquanto a condição `contador < 5` for verdadeira. A cada iteração, o valor de `contador` é impresso e incrementado em 1. O loop será executado cinco vezes, imprimindo os números de 0 a 4.

É importante garantir que a condição de parada seja eventualmente atingida em um loop `while`, caso contrário, o loop continuará indefinidamente, resultando em um loop infinito.

Ao usar os loops `for` e `while`, é possível controlar o fluxo de execução do programa e realizar operações repetitivas de forma eficiente.

Neste capítulo, exploramos a sintaxe básica da linguagem Python. Vimos a estrutura de um programa Python, os diferentes tipos de dados e operadores disponíveis, bem como as estruturas de controle de fluxo, como condicionais (`if/else`) e loops (`for/while`). No próximo capítulo, continuaremos a construir sua base em Python3, explorando estruturas de dados e funções.