# Capítulo 4: Manipulação de Arquivos e Exceções

## Manipulando Arquivos

Trabalhar com arquivos é uma tarefa comum na programação, e o Python oferece várias funcionalidades para ler e escrever dados de e para arquivos. Em Python, você pode usar a função embutida `open()` para abrir um arquivo e realizar operações nele.

### Abrindo um Arquivo

Para abrir um arquivo, você precisa especificar o nome do arquivo e o modo no qual deseja abri-lo. O modo pode ser "r" para leitura, "w" para escrita, "a" para adicionar conteúdo, ou "x" para criar um novo arquivo. O modo padrão é "r" se não for especificado.

```python
arquivo = open("exemplo.txt", "r")
```

Neste exemplo, abrimos um arquivo chamado "exemplo.txt" no modo de leitura e atribuímos à variável `arquivo`. O arquivo deve existir no local especificado.

### Leitura de um Arquivo

Depois de abrir um arquivo, você pode realizar várias operações nele. Para ler o conteúdo de um arquivo, você pode usar o método `read()`, que lê o arquivo inteiro ou um número específico de caracteres.

```python
arquivo = open("exemplo.txt", "r")
conteudo = arquivo.read()
print(conteudo)
```

Este código lê o conteúdo inteiro do arquivo e o atribui à variável `conteudo`. Em seguida, ele imprime o conteúdo no console.

### Escrita em um Arquivo

Para escrever dados em um arquivo, você precisa abri-lo no modo de escrita ("w"). Esse modo sobrescreve o arquivo se ele já existir ou cria um novo arquivo se não existir.

```python
arquivo = open("exemplo.txt", "w")
arquivo.write("Olá, Mundo!")
arquivo.close()
```

Neste exemplo, abrimos o arquivo no modo de escrita, escrevemos a string "Olá, Mundo!" nele e depois fechamos o arquivo. O conteúdo anterior do arquivo, se houver, será substituído.

### Adição de Conteúdo em um Arquivo

Se você deseja adicionar conteúdo a um arquivo existente sem sobrescrevê-lo, você pode abrir o arquivo no modo de adição ("a").

```python
arquivo = open("exemplo.txt", "a")
arquivo.write(" Adicionando novo conteúdo!")
arquivo.close()
```

Este código abre o arquivo no modo de adição, escreve a string " Adicionando novo conteúdo!" nele e fecha o arquivo. O novo conteúdo será adicionado ao final do arquivo.

### Fechando um Arquivo

Depois de terminar de trabalhar com um arquivo, é importante fechá-lo usando o método `close()`. Isso libera quaisquer recursos do sistema associados ao arquivo e garante que os dados sejam gravados corretamente.

```python
arquivo = open("exemplo.txt", "r")
conteudo = arquivo.read()
print(conteudo)
arquivo.close()
```

Neste exemplo, o arquivo é aberto, seu conteúdo é lido e impresso, e em seguida o arquivo é fechado.

## Lidando com Exceções e Erros

Em Python, exceções são disparadas quando ocorrem erros durante a execução do programa. Essas exceções podem ser tratadas usando blocos `try-except`, permitindo que você controle como o programa reage a esses erros.

### Blocos Try-Except

Um bloco `try-except` permite que você execute um código e capture exceções que possam ocorrer durante a execução. O código que pode gerar uma exceção é colocado dentro do bloco `try`, e o código que trata a exceção é colocado dentro do bloco `except`.

```python
try:
    # Código que pode gerar exceções
    valor = int(input("Digite um número: "))
    resultado = 10 / valor
    print(resultado)
except ZeroDivisionError:
    print("Erro: Divisão por zero!")
except ValueError:
    print("Erro: Entrada inválida!")
```

Neste exemplo, o código dentro do bloco `try` tenta obter um número do usuário e realizar uma divisão. Se ocorrer um `ZeroDivisionError` ou `ValueError`, o bloco `except` correspondente trata a exceção e imprime uma mensagem de erro.

### O Bloco Finally

O bloco `finally` é opcional e pode ser adicionado após os blocos `try-except`. Ele é executado independentemente se uma exceção ocorreu ou não. Geralmente, é usado para liberar recursos ou executar operações de limpeza.

```python
try:
    # Código que pode gerar uma exceção
    arquivo = open("exemplo.txt", "r")
    conteudo = arquivo.read()
    print(conteudo)
except FileNotFoundError:
    print("Erro: Arquivo não encontrado!")
finally:
    # Código que é sempre executado
    arquivo.close()
```

Neste exemplo, o bloco `try` tenta abrir e ler um arquivo. Se ocorrer um `FileNotFoundError`, o bloco `except` trata a exceção e imprime uma mensagem de erro. O bloco `finally` garante que o arquivo seja fechado, independentemente se ocorreu uma exceção ou não.

## Melhores Práticas para Manipulação de Arquivos e Tratamento de Exceções

Ao trabalhar com arquivos e tratar exceções, considere as seguintes melhores práticas:

- Use o comando `with`: O comando `with` cuida automaticamente do fechamento do arquivo, mesmo se ocorrer uma exceção. É recomendado para operações com arquivos.

```python
with open("exemplo.txt", "r") as arquivo:
    conteudo = arquivo.read()
    print(conteudo)
```

- Trate exceções específicas: Capture exceções específicas sempre que possível para fornecer mensagens de erro mais significativas e lidar com diferentes tipos de exceção de maneira diferente.

- Evite tratamento amplo de exceções: Evite usar um bloco `except` genérico sem especificar o tipo de exceção. Isso pode dificultar a depuração e compreensão do código.

- Limpe os recursos: Certifique-se de que quaisquer recursos, como arquivos abertos ou conexões, sejam fechados ou liberados corretamente, mesmo em caso de exceção.

Seguindo essas práticas, você pode escrever um código robusto que lida com erros de maneira adequada e evita vazamentos de recursos.

Neste capítulo, você aprendeu sobre a manipulação de arquivos e o tratamento de exceções em Python. Você descobriu como ler e escrever dados em arquivos, bem como como lidar com exceções para garantir que seu programa se comporte corretamente, mesmo em situações de erro. No próximo capítulo, continuaremos explorando mais tópicos importantes em Python.