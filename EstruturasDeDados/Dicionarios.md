## Dicionários ou dictionaries

Os dicionários são outra de forma de armazenar dados e usando as chaves para criar um dicionário, podemos até mesmo armazenar dicionário de dicionários. Os dicionários possuem uma chave e um valor:

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    
    dicio = {
        "Casa": "Vermelha",
        "bola": [2, "azul"],
        "carro": ["4 portas", "vermelho"]
    }

Os dicionários tem ordem, são mutáveis e não permitem chaves duplicadas.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'gato'}
        
Podemos ver o tamanho do dicionário com a função **len()**:

**Exemplo:**
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(len(dicio))
    saída:
    3
Ao colocar a mesma chave em um dicionário a nova chave vai sobrescrever a anterior

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato",
        3: "hamster"
    }
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'hamster'}
    
### Dicionário Construtor

Podemos usar o **dict()** para criar um dicionário:

**Exemplo:**

    dicio = dict(cachoro = "marrom", gato = "preto", hamster = "branco")
    print(dicio)
    saída:
    {'cachoro': 'marrom', 'gato': 'preto', 'hamster': 'branco'}    
    
### Acessar elementos de um dicionário

Para acessar um elemento de um dicionário usamos usar os colchetes passando o nome da chave.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(dicio[1])
    saída:
    cachorro

Também podemos usar o método **get()**.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(dicio.get(1))
    saída:
    cachorro

Usamos o método **keys()** para pegar todas as chaves do dicionário:

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(dicio.keys())
    saída:
    dict_keys([1, 2, 3])

Ao usar o método **keys()** e passar o resultado a uma variável caso o dicionário seja modificado a variável com as chaves também será modificada

**Exemplo:**
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    
    x = dicio.keys()
    
    print(x) 
    saída:
    dict_keys([1, 2, 3])
    
    dicio[4] = "hamster"
    
    print(x)
    saída:
    dict_keys([1, 2, 3, 4])
    
Com o método **values()* podemos pegar todos os valores dentro do dicionário

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(dicio.values())
    saída:
    dict_values(['cachorro', 'cavalo', 'gato'])
    
Com o método **items()** podemos cada elemento dentro do dicionário

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    print(dicio.items())
    saída:
    dict_items([(1, 'cachorro'), (2, 'cavalo'), (3, 'gato')])

Podemos também verificar se certo elemento existe dentro do dicionário usando o **in**.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    if "gato" in dicio.values():
        print("Há um gato dentro do dicionário")
    saída:
    Há um gato dentro do dicionário

    
### Mudando valores do dicionário

Para mudar o valor de um elementento específico podemos passar o valor da chave entre colchetes.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio[3] = "hamster"
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'hamster'}
    
Podemos usar o método **update()** para atualizar valores dentro do dicionário.
**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio.update({3: "hasmter"})
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'hasmter'}
    
### Adicionando elementos ao dicionário.

Para adicionar um novo elemento ao dicionário podemos
passar uma nova chave e adicionar um valor a ela.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio[4] = "hamster"
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'gato', 4: 'hamster'}

Também podemos usar o método **update()** como já foi mostrado anteriormente.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio.update({4: "hamster"})
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'gato', 4: 'hamster'}
    
### Removendo elementos do dicionário

Há diversas maneiras de remover elementos do dicionário.

Podemos utilizar o método **pop()** para remover um elemento com uma chave específica.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio.pop(2)
    print(dicio)
    saída:
    {1: 'cachorro', 3: 'gato'}

Podemos utilizar método **popitem()** remove o último elemento inserido.

**Exemplo:**    
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio.popitem()
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo'}

Podemos utilizar o **del** para remover um elemento passando uma chave específica.

**Exemplo:**
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    del dicio[3]
    print(dicio)
    saída:
    {1: 'cachorro', 2: 'cavalo'}

Podemos utilizaro **del** para deletar o dicionário completamente também.

**Exemplo:**
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    del dicio
Se tentarmos printar o dicio agora vai dar um erro, porque ele não existe mais na memória.

Podemos usar o **clear()** para esvaziar o dicionário:

**Exemplo**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio.clear()
    print(dicio)
    saída:
    {}

### Laços ou loops em dicionários
    
Podemos fazer loops em dicionários utilizando o **for**.<br>
Ao fazer um loop em um dicionário irá nos mostrar as chaves, mas tem métodos para retonar os valores também.

**Exemplo:**
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    for x in dicio:
        print(x)
    saída:
    1
    2
    3
    
Para mostrar os valores:

**Exemplo:**
    
    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    for x in dicio:
        print(dicio[x])
    saída:
    cachorro
    cavalo
    gato

Támbem podemos usar o método **values()** para retornar os valores:
    
**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    for x in dicio.values():
        print(x, end=" ")
    saída:
    cachorro, cavalo, gato
    
Podemos usar o método **keys()** para retonar as chaves do dicionário.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    for x in dicio.keys():
        print(x, end=" ")
    saída:
    1 2 3 

Podemos retonar as chaves e os valores ao mesmo tempo
usando o método **items()**.

**Exemplo:**

    dicio = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    for x, y in dicio.items():
        print(x, y)
    saída:
    1 cachorro
    2 cavalo    
    3 gato

### Copiar um dicionário

Não podemos copiar um dicionário digitando dicio1 = dicio2, porque vamos criar uma referência de memória
ao dicio1, todas as mudanças que foram feitas no dicio1 serão refletidas também no dicio2. <br>
Outra de forma de copiar um dicionário é utilizando o método **copy()**.

**Exemplo:**

    dicio1 = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio2 = dicio1.copy()
    print(dicio2)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'gato'}
    
Outra forma de copiar o dicionário é utilizando o **dict()**.

**Exemplo:**

    dicio1 = {
        1: "cachorro",
        2: "cavalo",
        3: "gato"
    }
    dicio2 = dict(dicio1)
    print(dicio2)
    saída:
    {1: 'cachorro', 2: 'cavalo', 3: 'gato'}

