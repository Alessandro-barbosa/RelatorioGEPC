
## Listas ou lists

As listas em python são formas de armazenar dados em uma variável, essas listas podem armazenar dados de diferentes tipos em uma mesma variável, como inteiro, ponto flutuante, string e booleano.
Os elementos em uma lista possuem posições, são mutáveis e podem ser iguais. <br>
As listas são criadas usando colchetes.

**Exemplo:**

    lista1= ["manga", "abacate", "banana"]
    lista2 = [1, 10, 3]
    lista3 = [1.5, 10.5, 2.5]
    lista4 = ["manga", "banana", 1, 1.5, True]
        
### Acesso a elementos de uma Lista:

Os elementos em uma lista tem posições:
    
**Exemplo:**

    lista = ["morango", "uva", "azeitona"]
    print(lista[1])
    saída:
    uva    
    
A saída foi o elemento da posição 1: "uva", pois o primeiro elemento tem o índice 0.
	
Também é possível ter como referência índices negativos que começam do final pro começo.
-1 refere-se ao último item da lista enquando -2 refere-se ao segundo último elemento:

**Exemplo:**    
    
    lista = ["morango", "uva", "azeitona"]
    print(lista[-1])
    saída:
    azeitona
    
enquanto o comando:
    
    print(lista[-2])
    saída:
    uva
    
será o penúltimo elemento: "uva"

### Intervalo entre índices:

É possível também especificar um intervalo de começo e final de busca:

**Exemplo:**

    
	lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	print(lista[1:4])
    saída:
    ['uva', 'azeitona', 'maça']
    
    
A quarta posição não é incluída, lembrando que o primeiro índice começa em 0;
Da mesma forma que é possível apenas definir apenas o limite final:
    
    lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	print(lista[:4])
	saída:
    ['morango', 'uva', 'azeitona', 'maça']
    
Também é possível definir por onde deve começar:

    lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	print(lista[3:])
	saída:
    ['maça', 'banana', 'melancia']

### Verificar um elemento dentro da lista:

Para verificar se existe algum elemento dentro de uma lista, podemos usar o **in**:

**Exemplo:**

	lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	if "uva" in lista:
        print("Há uva na lista")
    else:
        print("Não há uva na lista")
	saída:
    Há uva na lista
    
    

### Mudando elementos de uma lista:

É possível mudar elementos de com um índice:

	lista = ["morango", "uva", "melancia"]
	lista[0] = "banana"
    print(lista)
	saída:
    ['banana', 'uva', 'melancia']
    
O código mudou o elemento do índice 0.

### Inserindo elementos em uma lista:

Para inserir um elemento em uma lista podemos utilizar o método **insert()**.

**Exemplo:**    

	lista = ["morango", "uva", "melancia"]
	lista.insert(0, “banana”) 
    print(lista)
    saída:
    ['banana', 'morango', 'uva', 'melancia']
    
O código inseriu um novo elemento no índice 0 e o antigo elemento na posição 0 será deslocado a frente para o índice 1.

Para adicionar um elemento no final da lista, podemos usar o método **append()**.

**Exemplo:**
    
    lista = ["morango", "uva", "melancia"]
    lista.append("banana")
    print(lista)
    saída:
    ['morango', 'uva', 'melancia', 'banana']
    
O código adicionou um novo elemento ao final da lista.
    
Podemos também extender uma lista a partir de outra lista para isso podemos utilizar o método **extend()**.
    
**Exemplo:**

    lista1 = ["morango", "uva", "melancia"]
    lista2 = ["abacate", "pessego", "maça"]
    lista1.extend(lista2)
    print(lista1)
    saída:
    ['morango', 'uva', 'melancia', 'abacate', 'pessego', 'maça']
    
O código extendeu a lista2 para a lista1 gerando uma lista maior!.
    
### Remover elementos de uma lista

Com o método **remove()** podemos remover um item caso exista dentro da lista.
    
**Exemplo:**
    
    lista = ["morango", "uva", "melancia"]
    lista.remove("morango") 
    print(lista)
    saída:
    ['uva', 'melancia']

O comando removeu o primeiro elemento encontrado passado no método.
    
Com o método **pop()** podemos remover um elemento em certo índice passado no método.
    
**Exemplo:**

    lista = ["morango", "uva", "melancia"]
    lista.pop(2)
    print(lista)
    saída:
    ['morango', 'uva']
    
irá remover o elemento do índice 2.
Caso não seja especificado um índice ao método **pop()** será removido o último elemento da lista.

O del também remove um elemento da lista:
    
**Exemplo:**

    lista = ["morango", "uva", "melancia"]
    del lista[0]
    print(lista)
    saída:
    ['uva', 'melancia']
    
O comando irá remover o elemento do índice 0.
Com o del também podemos deletar uma lista inteira:
    
    lista = ["morango", "uva", "melancia"]
    del lista
    
Esse método remove a variável da memória!

Com o método **clear()** podemos esvaziar a lista. A lista continua a existir, mas ela não tem mais conteúdo.

**Exemplo:**

    lista: ["morango", "uva", "melancia"]
    lista.clear()
    print(lista)
    saída:
    []
    
### Laços ou loops em listas

Você pode percorrer elementos de uma lista usando o **for**:
    
**Exemplo:**

    lista = ["morango", "uva", "melancia", "morango"]
    contador = 0
    for x in lista:
        if x == "morango":
            contador += 1
    if contador > 0:
        print(f"Há {contador} morangos na lista")
    else:
        print("Não há morangos na lista")
    saída:
    Há 2 morangos na lista
    
O código nos retornou a quantidade de morangos que existem dentro da lista, caso eles existam dentro da lista.

Podemos também percorrer a lista passando um índice. Usamos o *range()** e o **len()** para fazer isso.
A combinção dos dois faz com que consigamos percorrer a lista do índice 0 até o tamanho máximo dela.
    
**Exemplo:**

    lista = ["morango", "uva", "melancia"]
    for x in range(len(lista)):
        print(lista[x], end = " ")
    saída:
    morango uva melancia

O código ira percorrer a lista pelo tamanho dela mostrando os elementos conforme os índices. O código: (end = " ") vai imprimir os elementos na mesma linha com um espaço entre elas. 

Também podemos usar o while para laços:
    
**Exemplo:**

    lista = ["morango", "uva", "melancia"]
    i = 0
    while i < len(lista):
        print(lista[i], end = " ")
        i += 1
    saída:
    morango uva melancia
    
### List Comprehesion ou Compreensão De Lista

A compreensão de lista é uma forma de criar uma lista com poucas linhas de código.
Com uma lista existente podemos criar uma outra de acordo com certos parâmetros:
    
**Exemplo:**
    
    lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    listaNumeros = []
    for x in lista:
        if x > 4:
            listaNumeros.append(x)
    print(listaNumeros)
    saída:
    [5, 6, 7, 8, 9, 10]
    
Ou podemos usar o list comprehesion para reduzir o código.
    
    lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    listaNumeros = [x for x in lista if x > 4]
    print(listaNumeros)
    saída:
    [5, 6, 7, 8, 9, 10]
    
Sintaxe: 

    lista = [expressão for item in iterador if condição == Verdade]
    
Expressão: é a variável que irá entrar na nova lista, sendo possível manipular-lá antes de ela realmente entrar na lista. <br>
Iterador: pode ser qualquer objeto, como uma lista, conjunto, funções, etc.<br>
Condição: Lógica para o elemento entrar na lista.

### Ordenação de listas

As listas tem o método **sort()** que vai ordenar a lista, seja em ordem alfabética, númerica: crescente ou decrescente.
    
**Exemplo:**

    De forma crescente:
    lista = [10, 5, 6, 7, 1, 4, 0]
    lista.sort()
    print(lista)
    Saída:
    [0, 1, 4, 5, 6, 7, 10]

    Decrescente:
    lista = [10, 5, 6, 7, 1, 4, 0]
    lista.sort(reverse = True)
    print(lista)
    Saída:
    [10, 7, 6, 5, 4, 1, 0]

    Com string:
    lista = ["banana", "uva", "acerola", "melão"]
    lista.sort()
    print(lista)
    saída:
    ['acerola', 'banana', 'melão', 'uva']
