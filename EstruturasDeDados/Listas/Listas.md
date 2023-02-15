#Estruturas de Dados com Python

##Listas:
	As listas em python são formas de armazenar dados em uma variável, essas listas podem armazenar dados de diferentes tipos em uma mesma lista, como inteiros, float, strings e booleans.
	As listas são ordenadas, são mutáveis e permitem itens duplicados;
	As listas são criadas com colchetes:
    
	Exemplo
		lista1= ["manga", "abacate", "banana"]
		lista2 = [1, 10, 3]
		lista3 = [1.5, 10.5, 2.5]
		lista4 = ["manga", "banana", 1, 1.5, True]
        
###Acesso a elementos de uma Lista:
    Os elementos de um uma lista tem posições, sendo uma lista:
    
	Exemplo:
		lista = ["morango", "uva", "azeitona"]
		O comando -> print(lista[1])
		Vai ter como saída o elemento da posição 1: "uva", pois o primeiro elemento tem o índice 0.
	
	Também é possível ter como referência index negativos que começam do final pro começo;
	Exemplo:
		-1 refere-se ao último item da lista enquando -2 refere-se ao segundo do final pro começo:
		lista = ["morango", "uva", "azeitona"]
		O comando ->  print(lista[-1])
		Vai ter como saída o último elemento: "azeitona"
		enquanto o comando -> print(lista[-2])
		Vai ter como saída o segundo último elemento: "uva"

###Intervalo entre posições ou índices:
	É possível também especificar um intervalo de começo e final de busca:
	lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	O comando -> print(lista[1:4])		
	Vai ter como saída o as palavras: "uva", "azeitona", "maça". Pois está começando da posição 1 até a posição 3, a quarta posição não é incluída, lembrando que o primeiro índice começa em 0;
	Da mesma forma que é possível apenas definir apenas o limite final:
	-> print(lista[:4])
	a saída será: "morango", "uva", "azeitona", "maça". começando do índice 0 e indo até o índice 3
	Também é possível definir onde deve começar
	-> print(lista[3:])
	A saída será começando do índice 3 até o final: ['maça', 'banana', 'melancia']

###Checar se existe algum elemento na lista:
	Para checar se existe algum elemento dentro de uma lista, podemos usar o in:
	lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	O comando -> if "uva" in lista:
			print("Há uva na lista")
		     else:
			print("Não há uva na lista")
	A saída será: "Há uva na lista"

###Mudando elementos de uma lista:
	É possível mudar elementos de certo índice:
	lista = ["morango", "uva", "melancia"]
	O comando -> lista[0] = "banana", irá mudar o elemento do índice 0
	a nova lista será ["banana", "uva", "melancia"]

###Inserindo elementos em uma lista:
Para inserir um elemento em uma lista podemos utilizar o método insert().

    Exemplo:    
	lista = ["morango", "uva", "melancia"]
	O comando -> lista.insert(0, “banana”) vai inserir um novo elemento no índice 0 e o antigo elemento na posição 0 será deslocado a frente para o índice 1.

Para adicionar um elemento no final da lista, podemos usar o método append()

    Exemplo:
    lista = ["morango", "uva", "melancia"]
    O comando -> lista.append("banana") vai adicionar um novo elemento ao final da lista.
    A nova lista será lista = ["morango", "uva", "melancia", "banana"]
    
Podemos também extender uma lista a partir de outra lista
para isso podemos utilizar o método extend()
    
    Exemplo:
        lista1 = ["morango", "uva", "melancia"]
        lista2 = ["abacate", "pessego", "maça"]
        o comando -> lista1.extend(lista2) Ira extender a lista a lista2 na lista1 gerando uma lista maior.

###Remover elementos de uma lista
    Com o método remove() podemos remover um item caso exista dentro da lista.
    
    Exemplo:
        lista = ["morango", "uva", "melancia"]
        O comando -> lista.remove("morango") irá remover o primeiro elemento encontrado pasasdo no método.
    
    Com o método pop() podemos remover um elemento em certo índice passado no método.
    
    Exemplo:
        lista = ["morango", "uva", "melancia"]
        O comando -> lista.pop(0) irá remover o elemento do índice 0. a nova lista será:
        lista = ["uva", "melancia"]
        
    Caso não seja especificado um índice ao método pop() será removido o último elemento da lista.

    O del também remove um elemento da lista:
    
    Exemplo:
        lista = ["morango", "uva", "melancia"]
        O comando -> del lista[0] irá remover o elemento do índice 0.
    Com o del também podemos deletar uma lista inteira:
    
    Exemplo:
        lista = ["morango", "uva", "melancia"]
        del lista

    Com o método clear() esvazia a lista. A lista continua a existir porém ela não tem mais conteúdo.
    
## Laços em listas
Você pode percorrer elementos de uma lista usando o for:
    
    Exemplo:
        lista = ["morango", "uva", "melancia", "morango"]
        contador = 0
        for x in lista:
            if x == "morango":
                contador += 1
        if contador > 0:
            print(f"Há {contador} morangos na lista")
        else:
            print("Não há morangos na lista")
    O código irá retonar a quantidade de morangos que existem dentro da lista, caso eles existam dentro da lista.

Podemos também percorrer a lista conforme a quantidade de elementos dela. Usamo o range() e o len() para fazer isso.
A combinção dos dois faz com que consigamos percorrer a lista do índice 0 até o tamanho máximo dela.
    
    Exemplo:
        lista = ["morango", "uva", "melancia"]
        for x in range(len(lista)):
            print(x, end = " ")
    O código ira percorrer a lista pelo tamanho dela dando os índices da mesma. A parte do código: (end = " ") irá imprimir os elementos na mesma linha com um espaço. 
    
Também podemos usar o while para laços:
    
    Exemplo:
        lista = ["morango", "uva", "melancia"]
        i = 0
        while i < len(lista):
            print(lista[i])
            i += 1
            
##List Comprehesion ou Compreensão De Lista

A compreensão de lista é uma forma de criar uma lista com poucas linhas de código.
Com uma lista existente podemos criar uma outra de acordo com certos parâmetros:
    
    Exemplo:
        lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        listaNumeros = [x for x in lista if x > 4]
        print(listaNumeros)
        Saída -> [5, 6, 7, 8, 9, 10]
        
    O código de outr forma:
        lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        listaNumeros = []
        for x in lista:
            if x > 4:
                listaNumeros.append(x)
        print(listaNumeros)
        
Sintaxe: 
    lista = [expressão for item in iterador if condição == Verdade]
Expressão é a variável que irá entrar na nova lista, sendo possível manipular-lá antes de ela realmente entrar na lista.
Iterador pode ser qualquer objeto, como uma lista, conjunto, funções, etc.

##Ordenação de listas

As listas tem o método sort() que irá organizar a lista, seja em ordem alfabética, númerica: crescente ou decrescente.
    
    Exemplo:
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
        
