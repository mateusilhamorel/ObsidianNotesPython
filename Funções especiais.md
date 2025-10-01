Sintaxe


Lambda
Em **Python**, uma **função `lambda`** é uma forma curta (anônima) de declarar funções simples, geralmente em **uma única linha**.

```python
lambda argumentos: expressão

```

- **`lambda`** → palavra-chave para criar a função.
- **`argumentos`** → parâmetros que a função recebe (pode ser nenhum, um ou vários).
- **`expressão`** → o valor que será retornado (não precisa escrever `return`).

Exemplo:
```python
quadrado = lambda x: x * x
print(quadrado(5))  # saída: 25

```


Filter

Em uma Filtragem uma função é aplicada em uma lista de itens de um sequência
Se o item que retornar for verdadeiro ele fará parte da nova lista 
Se for falso, não entrará na nova lista
A lista resultante pode não ter o mesmo tamanho da original, sendo menor.
Usamos filter para filtrar uma lista:

```python
lista = [1,2,3,4,5,6,7,8,9,10]

print("Da lista lista = [1,2,3,4,5,6,7,8,9,10]")
print("Filtrar os impares")

impares = filter(lambda x: x % 2, lista)

print(list(impares))
```

- `filter()` é uma função que recebe:
    - uma **função** (nesse caso, `lambda x: x % 2`),
    - um **iterável** (nesse caso, `lista`).
        
- O `lambda x: x % 2` devolve:
    - `0` se o número for par,
    - `1` se o número for ímpar.
        
- O `filter()` mantém apenas os elementos da lista para os quais a função retorna um valor considerado **True**.
    - Em Python, `0` é considerado **False** e qualquer outro número é **True**.
    - Logo, **só passam os ímpares**.


Map

Map consiste em aplicar uma função a todos os itens de uma lista;
Gera outra sequência com os resultados (mesmo tamanho da sequência inicial).

```python
print("Gerar uma lista de numeros com -> nums = range(0,11)")

nums = range(0,11)
print("Agora vamos usar o map e uma lambda pra dividir cada numero por 3")

print("list(map(lambda x: x / 3, nums))")
print(list(map(lambda x: x / 3, nums)))
```


Reduce

Redução é feita com reduce do pacote functools.
Ela recebe dois parâmetros e aplica uma função.
A primeira iteração são os dois primeiros itens da lista.
A próxima interação é o próximo item da lista com o resultado anterior.

```python
from functools import reduce

lista = [1,2,3,4,5,6,7]
soma = reduce(lambda x,y: x+y, lista)
print(soma)
```



Transposição (zip)

Transposição é construir uma SERIE de SEQUENCIAS a partir de OUTRA SERIE de SEQUENCIAS.
A primeira nova sequência é composta do primeiro elemento das sequencias originais.
A segunda nova sequencia é formada pelo segundo elemento das sequencias originais. E assim por diante.

Exemplo:


```python
A = [1,2,3,4,5]
B = [6,7,8,9,10]
C = [11,12,13,14,15]
D = [16,17,18,19,20]
E = [21,22,23,24,25]


print(list(zip(A, B, C, D, E)))
```

Explicando um pouco melhor:
A função **`zip()`** combina elementos de várias listas (ou outros iteráveis) **posição a posição**.
- O primeiro elemento de cada lista vira uma **tupla**.
- Depois o segundo de cada lista, e assim por diante.
- Para quando a menor lista acaba.

O resultado do código acima é o seguinte:

```python
[(1, 6, 11, 16, 21),
 (2, 7, 12, 17, 22),
 (3, 8, 13, 18, 23),
 (4, 9, 14, 19, 24),
 (5, 10, 15, 20, 25)]
```

