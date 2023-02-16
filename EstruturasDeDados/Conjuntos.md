
## Conjunto ou set

Outra estrutura de dados capaz de armazenar vários elementos em uma variável, sendo inteiro, string, ponto flutuante.<br>
Os elementos dos conjuntos não possuem ordem, são imutáveis, e sem índice. Mesmo os elementos sendo imutáveis ainda é possível remover elementos e adicionar também.<br>
Para representar um conjunto usamos as chaves

**Exemplo:**

    conjunto = {"uva","melancia","banana"}
    print(conjunto)
    saída:
    {'melancia', 'banana', 'uva'}      
    
**Toda vez que for impresso um set os valores podem mudar de ordem**

Nos conjuntos não é possível haver elementos duplicados!

### Tamanho de um conjunto

Podemos usar a função **len()** para saber tamanho de um
conjunto.

**Exemplo:**

    conjunto = {"uva","melancia","banana"}
    print(len(conjunto))
    saída:
    3

### Construtor do conjunto

Podemos também usar o **set()** para fazer um conjunto.

**Exemplo:**
    
    conjunto = set(("uva","melancia","banana"))
    print(conjunto)
    saída:
    {'banana', 'melancia', 'uva'}

### Métodos de acesso em um conjunto

Como os conjuntos não possuem posições corretas
não podemos acessar aos elementos passando índices.<br>
Para acessar os elementos de um conjunto podemos usar o **for** com o **in**

**Exemplo:**

    conjunto = {"uva", "melancia", "banana"}
    for x in conjunto:
        print(x)
    saída:
    uva
    banana
    melancia

lembrando toda vez que um conjunto for impresso os elementos podem ser aparecer em ordem diferentees.

### Adicionado elementos a um conjunto

Quando um conjunto é criado os elementos já existentens não podem ser mudados, mas podemos adicionar novos. <br>
Usamos o método **add()** para adicionar novos elementos a um conjunto.

**Exemplo:**

    conjunto = {"uva", "melancia", "banana"}
    conjunto.add("manga")
    print(conjunto)
    
    saída:
    {'uva', 'manga', 'banana', 'melancia'} 

Podemos também adicionar outros conjuntos a outro conjunto o método **update()**.

**Exemplo:**

    conjunto1 = {"uva", "melancia", "banana"}
    conjunto2 = {1,2,3}
    conjunto1.update(conjunto2)
    print(conjunto1)
    
    saída:
    {1, 2, 'uva', 'melancia', 3, 'banana'}
    
Da mesma forma podemos adicionar outras estruturas de dados a um conjunto usando o mesmo método.

**Exemplo:**
    
    conjunto = {"uva", "melancia", "banana"}
    lista = ["maça", "morango"]
    conjunto.update(lista)
    print(conjunto)
    
    saída:
    {'maça', 'melancia', 'uva', 'morango', 'banana'}

### Removendo elementos de um conjunto

Para remover elementos de um conjunto podemos usar os métodos **remove()** ou o **discard()**.

**Exemplo:**

    conjunto = {"uva", "melancia", "banana"}
    conjunto.remove("uva")
    print(conjunto)
    
    saída:
    {'melancia', 'banana'}
    
usando o discard:

    conjunto = {"uva", "melancia", "banana"}
    conjunto.discard("uva")
    print(conjunto)
    
    saída:
    {'melancia', 'banana'}

A diferença entre os métodos **remove()** e o **discard()**
é que o **remove()** caso não tenha o valor passado como parâmetro vai acontecer um erro!.

Podemo usar o método **pop()** também, mas como os valores não possuem ordem certa, acontece de remover um item aleatório.

Podemos usar o **clear()** para limpar o conjunto.

**Exemplo:**

    conjunto = {"uva", "melancia", "banana"}
    conjunto.clear()
    print(conjunto)
    
    saída:
    set()
    
Com o del podemos deletar o conjunto completamente:

**Exemplo:**
    
    conjunto = {"uva", "melancia", "banana"}
    del conjunto    
    print(conjunto)
    
    saída:
    Irá acontecer um erro pois o conjunto não existe mais!
    
### Laços ou loops em conjuntos

Podemo fazer loops em conjuntos usando o **for**.

**Exemplo:**
    
    conjunto = {"uva", "melancia", "banana"}
    for x in conjunto:
        print(x)
    
    saída:
    uva
    melancia
    banana

### Junção de conjuntos

Podemo fazer a união de conjuntos usando os métodos **union()** ou o **update()**. <br>
O método **union()** cria um novo conjunto com todos os elementos de ambos os conjuntos

**Exemplo:**
    
    conjunto1 = {"uva", "melancia", "banana"}
    conjunto2 = {"manga", "melão", "manga"}
    conjunto3 = conjunto1.union(conjunto2)
    print(conjunto3)
    
    saída:
    {'uva', 'melão', 'manga', 'banana', 'melancia'}
    
enquanto o **update()** insere os elementos no conjunto.

**Exemplo:**
    
    conjunto1 = {"uva", "melancia", "banana"}
    conjunto2 = {"manga", "melão", "manga"}
    conjunto1.update(conjunto2)
    print(conjunto1)
    
    saída:
    {'banana', 'manga', 'uva', 'melancia', 'melão'}

Como estamos falando de conjuntos temos métodos para fazer a interseção e a diferença entre eles. <br>
Com o método **intersection()** teremos um novo conjunto apenas com os elementos que possuem nos outros conjuntos.

**Exemplo:**
    
    conjunto1 = {"uva", "melancia", "banana"}
    conjunto2 = {"uva", "melão", "manga"}
    conjunto3 = conjunto1.intersection(conjunto2)
    print(conjunto3)
    
    saída:
    {'uva'}    

Com o método **symmetric_difference_update()** deixamos apenas os elemetos que não estão presentes ao mesmo tempo nos conjuntos.


**Exemplo:**
    
    conjunto1 = {"uva", "melancia", "banana"}
    conjunto2 = {"uva", "melão", "banana"}
    conjunto1.symmetric_difference_update(conjunto2)
    print(conjunto1)
    
    saída:
    {'melancia', 'melão'}

O método **symmetric_difference()** que é parecido com o comando anterior, porém esse método cria um novo conjunto.

**Exemplo:**
    
    conjunto1 = {"uva", "melancia", "banana"}
    conjunto2 = {"uva", "melão", "banana"}
    conjunto3 = conjunto1.symmetric_difference(conjunto2)
    print(conjunto3)
    
    saída:
    {'melancia', 'melão'}
