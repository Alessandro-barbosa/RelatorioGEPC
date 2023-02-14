#Estruturas de Dados python
Listas:
	As listas em python são formas de armazenar dados em uma variável, essas listas podem armazenar dados de diferentes tipos em uma mesma lista, como inteiros, float, strings e booleans;
	As listas são ordenadas, são mutáveis e permitem itens duplicados;
	As listas são criadas com colchetes:
	Exemplo
		lista1= ["manga", "abacate", "banana"]
		lista2 = [1, 10, 3]
		lista3 = [1.5, 10.5, 2.5]
		lista4 = ["manga", "banana", 1, 1.5, True]
    
Acesso a elementos de uma Lista:
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

Intervalo entre posições ou índices:
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

Checar se existe algum elemento na lista:
	Para checar se existe algum elemento dentro de uma lista, podemos usar o in:
	lista = ["morango", "uva", "azeitona", "maça", "banana", "melancia"]
	O comando -> if "uva" in lista:
			print("Há uva na lista")
		     else:
			print("Não há uva na lista")
	A saída será: "Há uva na lista"

Mudando elementos de uma lista:
	É possível mudar elementos de certo índice:
	lista = ["morango", "uva", "melancia"]
	O comando -> lista[0] = "banana", irá mudar o elemento do índice 0
	a nova lista será ["banana", "uva", "melancia"]

Inserindo elementos em uma lista:
	Para inserir um elemento em uma lista podemos utilizar o método insert().
	lista = ["morango", "uva", "melancia"]
	O comando -> lista.insert(0, “banana”) vai inserir um novo elemento na lista mudando a posição do elemento do índice 0 e o deslocando a frente.
