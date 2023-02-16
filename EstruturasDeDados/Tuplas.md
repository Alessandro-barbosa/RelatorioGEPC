## tuplas ou tuples

É uma estrutura de dados capaz de armazenar vários dados em uma única variável. Podemos ter qualquer tipo de dado nas tuplas, seja string, números, booleanos. <br>
Em uma tupla dados tem ordem, podem ser repetidos e não podem ser mudados após a criação dela, mas existem formas de serem manipuladas para mudarmos os elementos. <br>
São criadas usando parênteses.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    tupla2 = (1, 10, 3)
    tupla3 = (1.5, 10.5, 2.5)
    tupla4 = ("uva", "banana", 1, 1.5, True)   

Podemos saber o tamanho da tupla com a função **len()**.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    print(len(tupla))
    saída:
    3
    
A criação da tupla com apenas um único item possui um problema
caso coloquemos:

    tupla = ("manga")
    print(type(tupla))
    saída:
    <class 'str'>
    
Ela será um Objeto str e não uma tupla, para mudarmos isso podemos fazer da seguinte forma:

    tupla = ("manga", )
    print(type(tupla))
    saída:
    <class 'tuple'>
    
Ou também:
    
    tupla = tuple(("manga"))
    print(type(tupla))
    saída:
    <class 'tuple'>
    
### Acesso a elementos de uma tupla

Podemos acessar os elementos da tupla passando o índice dentro de colchetes.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    print(tupla[1])
    saída:
    melancia

**Lembrando que o primeiro índice começa no 0**!

Também temos o acesso por índices negativos, **os índices negativos vão do final para o começo!**.<br>
-1 é para o último item, -2 para o segundo último item.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    print(tupla[-1])
    saída:
    banana

### Intervalo entre índices

Podemos especificar um intervalo de índices de onde queremos começar e onde queremos que termine o intervalo.

**Exemplo:**

    tupla = ("uva", "melancia", "banana", "manga", "kiwi")
    print(tupla[2:4])
    saída:
    ('banana', 'manga')

Podemos também apenas definir onde começa o intervalo.

**Exemplo:**

    tupla =("uva", "melancia", "banana", "manga", "kiwi")
    print(tupla[2:])
    saída:
    ('banana', 'manga', 'kiwi')

Do mesmo modo podemos definir apenas onde termina o intervalo.

**Exemplo:**

    tupla =("uva", "melancia", "banana", "manga", "kiwi")
    print(tupla[:3])
    saída:
    ('uva', 'melancia', 'banana')

### Verificar um elemento dentro da tupla:

Podemos fazer essa verificação com a palavra **in**.

**Exemplo:**

    tupla =("uva", "melancia", "banana", "manga", "kiwi")
    if "uva" in tupla:
        print("Há uva nessa tupla")
    saída:
    Há uva nessa tupla

### Mudando elementos de uma tupla

Mesmo as tuplas sendo imútaveis, ainda é possível fazer modificações de outros jeitos.
Podemos transformar a tupla em uma lista para fazer modificações.

**Exemplo:**

    tupla =("uva", "melancia", "banana")
    lista = list(tupla)
    lista[0] = "manga"
    tupla = tuple(lista)
    print(tupla)
    saída:
    ('manga', 'melancia', 'banana')

Podemos adicionar um elemento transformando a tupla em uma lista e usar o método **append()**.

**Exemplo:**
    
    tupla = ("uva", "melancia", "banana")
    lista = list(tupla)
    lista.append("manga")
    tupla = tuple(lista)
    print(tupla)
    saída:
    ('uva', 'melancia', 'banana', 'manga')

Podemos adicionar uma tupla a uma tupla também.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    tupla2 = ("manga",)
    tupla += tupla2
    print(tupla)
    saída:
    ('uva', 'melancia', 'banana', 'manga')

Convertendo para uma lista também podemos remover elementos.

**Exemplo:**
    
    tupla = ("uva", "melancia", "banana")
    lista = list(tupla)
    lista.remove("uva")
    tupla = tuple(lista)
    print(tupla)
    saída:
    ('melancia', 'banana')
    
Com o del podemos deletar a tupla da memória.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    del tupla
    
Tentar printar tupla irá gerar um erro, pois ela não existe mais.

### Desempacotamento de tupla

Ao criar uma tupla estamos empacotando os dados dentro dela, mas também podemos voltar os elementos para variáveis, é o que chamamos de desempacotar.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    (a, b, c) = tupla
    print(a)
    print(b)
    print(c)
    saída:
    uva
    melancia
    banana
    
O numero de variáveis que vão receber a tupla precisa ser o mesmo número de elementos dentro da tupla, mas podemos usar o asterico * para definir que ela vai receber as quantidades restantes de elementos.

**Exemplo:**

    tupla = ("uva", "melancia", "banana", "morango")
    (a, b, *c) = tupla
    print(a)
    print(b)
    print(c)
    saída:
    uva
    melancia
    ['banana', 'morango']
    
### Laços ou loops em tuplas

Podemos fazer loops em tuplas usando o **for**.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    for x in tupla:
        print(x, end = " ")
    saída:
    uva melancia banana
    
### Loops em tuplas com índices

Podemos usar as funções **range()** e **len()** para criar um iterador para percorrer elementos dentro da tupla.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    for i in range(len(tupla)):
        print(tupla[i], end=" ")
    saída:
    uva melancia banana
    
Podemos também usar o **while** para percorrer uma tupla.

**Exemplo:**

    tupla = ("uva", "melancia", "banana")
    i = 0
    while i < len(tupla):
        print(tupla[i], end=" ")
        i += 1
    saída:
    uva melancia banana
