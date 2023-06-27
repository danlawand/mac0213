# Capítulo 3: Estruturas de Dados

## Listas, Tuplas e Dicionários

Em Python, existem várias estruturas de dados que permitem armazenar e organizar conjuntos de valores de diferentes maneiras. As estruturas de dados mais comuns são listas, tuplas e dicionários.

### Listas

Uma lista é uma coleção ordenada e mutável de elementos em Python. Ela é definida utilizando colchetes `[]` e os elementos são separados por vírgulas. As listas permitem armazenar diferentes tipos de dados em sequência.

Exemplo de criação de uma lista:

```python
frutas = ["maçã", "banana", "laranja"]
```

### Tuplas

Uma tupla é uma coleção ordenada e imutável de elementos em Python. Ela é definida utilizando parênteses `()` e os elementos são separados por vírgulas. As tuplas são semelhantes às listas, mas não podem ser modificadas após a sua criação.

Exemplo de criação de uma tupla:

```python
coordenadas = (10, 20)
```

### Dicionários

Um dicionário é uma coleção não ordenada de pares chave-valor em Python. Cada elemento do dicionário consiste em uma chave e um valor associado. Os dicionários são definidos utilizando chaves `{}` e os pares chave-valor são separados por vírgulas.

Exemplo de criação de um dicionário:

```python
aluno = {"nome": "João", "idade": 25, "curso": "Engenharia"}
```

## Manipulação de Elementos em Estruturas de Dados

### Listas e Tuplas

As listas e as tuplas permitem manipular seus elementos de diferentes maneiras.

- Acesso aos elementos: Os elementos de uma lista ou tupla podem ser acessados utilizando a indexação. O primeiro elemento possui índice 0, o segundo elemento possui índice 1 e assim por diante.

```python
frutas = ["maçã", "banana", "laranja"]
print(frutas[0])  # Saída: "maçã"
```

- Modificação de elementos: Nas listas, os elementos podem ser modificados atribuindo um novo valor a um índice específico. Já nas tuplas, como são imutáveis, não é possível modificar seus elementos após a criação.

```python
frutas[1] = "morango"  # Modifica o elemento de índice 1 na lista
print(frutas)  # Saída: ["maçã", "morango", "laranja"]
```

- Adição e remoção de elementos: Nas listas, é possível adicionar elementos utilizando o método `append()` para adicionar ao final ou o método `insert()` para adicionar em uma posição específica. Para remover elementos, utiliza-se o método `remove()` para remover um elemento específico ou `pop()` para remover um elemento com base no índice.

```python
frutas.append("uva")  # Adiciona "uva" ao final da lista
frutas.remove("maçã")  # Remove a string "maçã" da lista
print(frutas)  # Saída: ["morango

", "laranja", "uva"]
```

### Dicionários

A manipulação de elementos em dicionários envolve a utilização das chaves para acessar e modificar os valores associados.

- Acesso aos elementos: Os elementos de um dicionário são acessados utilizando a chave correspondente.

```python
aluno = {"nome": "João", "idade": 25, "curso": "Engenharia"}
print(aluno["nome"])  # Saída: "João"
```

- Modificação de elementos: Os valores associados às chaves podem ser modificados atribuindo um novo valor à chave correspondente.

```python
aluno["idade"] = 26  # Modifica o valor associado à chave "idade"
print(aluno)  # Saída: {"nome": "João", "idade": 26, "curso": "Engenharia"}
```

- Adição e remoção de elementos: Para adicionar um novo par chave-valor, basta atribuir um valor a uma nova chave. Para remover um par chave-valor, utiliza-se o comando `del` seguido da chave correspondente.

```python
aluno["matrícula"] = 12345  # Adiciona um novo par chave-valor ao dicionário
del aluno["curso"]  # Remove o par chave-valor com a chave "curso"
print(aluno)  # Saída: {"nome": "João", "idade": 26, "matrícula": 12345}
```

## Acesso e Iteração pelos Elementos

### Acesso em Listas e Tuplas

Para acessar e percorrer os elementos de uma lista ou tupla, você pode utilizar estruturas de controle de fluxo, como o loop `for` ou a indexação.

- Loop `for`: O loop `for` permite percorrer os elementos de uma lista ou tupla de forma simples e direta.

```python
frutas = ["maçã", "banana", "laranja"]

for fruta in frutas:
    print(fruta)
```

- Indexação: Você pode acessar os elementos de uma lista ou tupla individualmente utilizando a indexação.

```python
frutas = ["maçã", "banana", "laranja"]

print(frutas[0])  # Saída: "maçã"
print(frutas[1])  # Saída: "banana"
print(frutas[2])  # Saída: "laranja"
```

### Acesso em Dicionários

Para acessar e percorrer os elementos de um dicionário, você pode utilizar o loop `for` juntamente com os métodos `keys()`, `values()` ou `items()`.

- Loop `for` com `keys()`: O método `keys()` retorna uma lista com todas as chaves do dicionário.

```python
aluno = {"nome": "João", "idade": 25, "curso": "Engenharia"}

for chave in aluno.keys():
    print(chave)
```

- Loop `for` com `values()`: O método `values()` retorna uma lista com todos os valores do dicionário.

```python
aluno = {"nome": "João", "idade": 25, "curso": "Engenharia"}

for valor in aluno.values():
    print(valor)
```

- Loop `for` com `items()`: O método `items()` retorna uma lista de tuplas contendo os pares chave-valor do dicionário.

```python
aluno = {"nome": "João", "idade": 25, "curso": "Engenharia"}

for chave, valor in aluno.items():
    print(chave, valor)
```

Neste capítulo, você aprendeu sobre listas, tuplas e dicionários em Python. Exploramos como criar, manipular e percorrer essas estruturas de dados. Esses conceitos são fundamentais para o desenvolvimento de programas mais complexos em Python, permitindo armazenar e organizar informações de maneira eficiente. Nos próximos capítulos, abordaremos outros tópicos importantes para o seu aprendizado em programação com Python.




<!-- 
### Listas

- **Listas**: Coleções ordenadas e mutáveis de elementos.

Uma lista é uma estrutura de dados versátil e mutável que permite armazenar uma coleção ordenada de itens. Diferentemente das tuplas, as listas são mutáveis, o que significa que é possível adicionar, remover e modificar elementos após a criação da lista. As listas são definidas utilizando colchetes `[]` e os elementos são separados por vírgulas.


```python
# Exemplos de listas em Python
frutas = ["maçã", "banana", "laranja"]

# Acessando elementos da lista
primeira_fruta = frutas[0]

# Modificando elementos da lista
frutas[1] = "morango"

# Adicionando elementos à lista
frutas.append("abacaxi")
```


- **Criação de uma lista**: Uma lista pode ser criada utilizando colchetes `[]` e separando os elementos por vírgulas. Os elementos podem ser de qualquer tipo e uma lista pode conter elementos de tipos diferentes.

```python
# Exemplo de criação de uma lista em Python
lista1 = [1, 2, 3]
lista2 = ["maçã", "banana", "laranja"]
lista3 = [1, "maçã", True]
```

- **Acesso aos elementos de uma lista**: Os elementos de uma lista podem ser acessados utilizando a indexação, onde o primeiro elemento possui índice 0, o segundo elemento possui índice 1 e assim por diante. Também é possível usar índices negativos para acessar os elementos a partir do final da lista.

```python
# Exemplos de acesso aos elementos de uma lista
print(lista1[0])  # Saída: 1
print(lista2[1])  # Saída: "banana"
print(lista3[-1]) # Saída: True
```

- **Modificação de elementos em uma lista**: Ao contrário das tuplas, as listas são mutáveis, o que significa que é possível modificar seus elementos atribuindo um novo valor a um índice específico.

```python
# Modificando elementos em uma lista
lista1[0] = 10
print(lista1)  # Saída: [10, 2, 3]
```

Nesse exemplo, o primeiro elemento da lista `lista1` é modificado de 1 para 10.

- **Adição de elementos em uma lista**: É possível adicionar elementos a uma lista utilizando o método `append()` para adicionar um elemento ao final da lista, ou utilizando o método `insert()` para inserir um elemento em uma posição específica.

```python
# Adicionando elementos em uma lista
lista2.append("uva")  # Adiciona "uva" ao final da lista2
print(lista2)  # Saída: ["maçã", "banana", "laranja", "uva"]

lista3.insert(1, "laranja")  # Insere "laranja" na posição 1 da lista3
print(lista3)  # Saída: [1, "laranja", "maçã", True]
```

- **Remoção de elementos de uma lista**: Os elementos de uma lista podem ser removidos utilizando os métodos `remove()` para remover um elemento específico, `pop()` para remover um elemento com base no índice ou `del` para remover um elemento em um índice específico.

```python
# Removendo elementos de uma lista
lista2.remove("banana")  # Remove a string "banana" da lista2
print(lista2)  # Saída: ["maçã", "laranja", "uva"]

elemento = lista1.pop(1)  # Remove o elemento de índice 1 da lista1 e o retorna
print(lista1)  # Sa

ída: [10, 3]
print(elemento)  # Saída: 2

del lista3[0]  # Remove o elemento de índice 0 da lista3
print(lista3)  # Saída: ["laranja", "maçã", True]
```

- **Operações com listas**: As listas suportam várias operações, como concatenação, fatiamento e verificação de pertencimento.

```python
# Exemplos de operações com listas
lista1 = [1, 2, 3]
lista2 = ["a", "b", "c"]

lista3 = lista1 + lista2  # Concatenação de listas
print(lista3)  # Saída: [1, 2, 3, "a", "b", "c"]

sublista = lista3[2:5]  # Fatiamento de lista
print(sublista)  # Saída: [3, "a", "b"]

print("a" in lista2)  # Verificação de pertencimento
# Saída: True, pois o elemento "a" está presente na lista2
```

As listas são uma estrutura de dados fundamental em Python devido à sua capacidade de armazenar e manipular coleções de itens de forma flexível. Elas oferecem a possibilidade de adicionar, remover e modificar elementos, tornando-as adequadas para muitas aplicações diferentes.


### Tuplas

- **Tuplas**: Coleções ordenadas e imutáveis de elementos.

Uma tupla é uma estrutura de dados semelhante a uma lista, mas com a diferença fundamental de ser imutável, o que significa que seus elementos não podem ser modificados após a criação. Uma tupla é definida utilizando parênteses `()` ou apenas separando os elementos por vírgulas.

Aqui está uma explicação sobre como as tuplas funcionam em Python:

- **Criação de uma tupla**: Uma tupla pode ser criada utilizando parênteses `()` ou separando os elementos por vírgulas. Os elementos podem ser de qualquer tipo, e uma tupla pode conter elementos de tipos diferentes.

```python
# Exemplo de criação de uma tupla em Python
tupla1 = (1, 2, 3)
tupla2 = ("maçã", "banana", "laranja")
tupla3 = (1, "maçã", True)
```

- **Acesso aos elementos de uma tupla**: Os elementos de uma tupla podem ser acessados utilizando a indexação, da mesma forma que em uma lista. A indexação começa a partir do índice 0 para o primeiro elemento.

```python
# Exemplos de acesso aos elementos de uma tupla
print(tupla1[0])  # Saída: 1
print(tupla2[1])  # Saída: "banana"
print(tupla3[2])  # Saída: True
```

- **Imutabilidade das tuplas**: Uma vez criada, uma tupla não pode ser modificada. Isso significa que você não pode adicionar, remover ou alterar elementos em uma tupla existente.

```python
# Exemplo de tentativa de modificar uma tupla (resultará em um erro)
tupla1[0] = 10  # Erro: As tuplas são imutáveis
```

- **Operações com tuplas**: As tuplas suportam várias operações, como concatenação, multiplicação e verificação de pertencimento.

```python
# Exemplos de operações com tuplas
tupla1 = (1, 2, 3)
tupla2 = ("a", "b", "c")

tupla3 = tupla1 + tupla2  # Concatenação de tuplas
print(tupla3)  # Saída: (1, 2, 3, "a", "b", "c")

tupla4 = tupla1 * 3  # Multiplicação de tupla por um número inteiro
print(tupla4)  # Saída: (1, 2, 3, 1, 2, 3, 1, 2, 3)

print(2 in tupla1)  # Verificação de pertencimento
# Saída: True, pois o elemento 2 está presente na tupla1
```

- **Desempacotamento de tuplas**: É possível atribuir os elementos de uma tupla a variáveis individuais em um processo chamado desempacotamento de tuplas.

```python
# Exemplo de desempacotamento de tuplas
tupla = ("João", 25, "São Paulo")
nome, idade, cidade = tupla

print(nome)   # Saída: "João"
print(idade)  # Saída: 25
print(cidade) # Saída: "São Paulo"
```

O uso de tuplas é útil quando se deseja armazenar um conjunto de elementos imutáveis, como coordenadas geográficas, dados constantes ou itens que não devem ser modificados. As tuplas também podem ser retornadas por funções, permitindo que múltiplos valores sejam retornados e desempacotados facilmente.


### Dicionários

- **Dicionários**: Coleções de pares chave-valor, onde cada chave é única.

Um dicionário é uma estrutura de dados que armazena coleções de pares chave-valor. Cada elemento no dicionário consiste em uma chave única e o valor associado a essa chave. Os dicionários são úteis quando se deseja armazenar e recuperar valores com base em uma chave específica, em vez de uma posição numérica como em uma lista.

Aqui está uma explicação sobre como os dicionários funcionam em Python:

- **Criação de um dicionário**: Um dicionário pode ser criado usando chaves `{}` e separando cada par chave-valor com dois pontos `:`. As chaves podem ser qualquer tipo imutável, como strings, números ou tuplas. Os valores podem ser de qualquer tipo, como strings, números, listas, dicionários e até mesmo funções.

```python
# Exemplo de criação de um dicionário em Python
pessoa = {
    "nome": "João",
    "idade": 25,
    "cidade": "São Paulo"
}
```

- **Acessando valores de um dicionário**: Os valores de um dicionário podem ser acessados ​​usando as chaves correspondentes dentro de colchetes `[]` ou usando o método `get()`.

```python
# Exemplos de acesso aos valores de um dicionário
nome = pessoa["nome"]
idade = pessoa.get("idade")
```

No exemplo acima, `nome` receberá o valor associado à chave `"nome"` no dicionário `pessoa`, ou seja, a string `"João"`. O mesmo acontece com a variável `idade`. No entanto, quando usamos `get("idade")`, se a chave não existir, será retornado o valor `None` em vez de causar um erro.

- **Modificação de valores em um dicionário**: Os valores em um dicionário podem ser modificados atribuindo um novo valor à chave correspondente.

```python
# Modificando valores em um dicionário
pessoa["idade"] = 30
```

Nesse exemplo, o valor da chave `"idade"` no dicionário `pessoa` é atualizado para 30.

- **Adição de novos pares chave-valor**: Novos pares chave-valor podem ser adicionados a um dicionário atribuindo um valor a uma chave que ainda não existe no dicionário.

```python
# Adicionando novos pares chave-valor a um dicionário
pessoa["profissão"] = "Engenheiro"
```

Nesse caso, um novo par chave-valor é adicionado ao dicionário `pessoa`, com a chave `"profissão"` e o valor `"Engenheiro"`.

- **Remoção de pares chave-valor**: Pares chave-valor podem ser removidos de um dicionário usando o comando `del` seguido da chave correspondente.

```python
# Removendo um par chave-valor de um dicionário
del pessoa["cidade"]
```

Nesse exemplo, o par chave-valor associado à chave `"cidade"` é removido do dicionário `pessoa`.

Os dicionários em Python são uma estrutura de dados poderosa e flexível, permitindo o armazenamento eficiente de informações organizadas por chaves. Eles são amplamente usados ​​para mapear e recuperar informações de forma rápida e eficaz, tornando-os uma ferramenta valiosa para muitos tipos de problemas de programação.
 -->
