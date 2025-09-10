Sintaxe

A estrutura FOR é uma estrutura que permite executar a repetição controlada de comandos/processamento.

No PYTHON, o FOR trabalha de forma mais direta do que em outras linguagens.
O FOR no PYTHON itera sequencialmente sobre os itens de uma lista ou sequência. (Em outras linguagens a iteração do for é controlada definindo-se um índice e um critério de parada - falarei disso depois.)

Seguem algumas estruturas para estudo:

```python
words = ['cat', 'window', 'defenestrate']
for w in words:
    print(w, len(w))

  
# Create a sample collection
users = {'Hans': 'active', 'Éléonore': 'inactive', 'Jhon': 'active'}

  
# Strategy:  Iterate over a copy
for user, status in users.copy().items():
    if status == 'inactive':
        del users[user]

  

# Strategy:  Create a new collection
active_users = {}
for user, status in users.items():
    if status == 'active':
        active_users[user] = status


#Se você precisa iterar sobre sequências numéricas,
# a função embutida range() é a resposta. Ela gera progressões aritméticas:
for i in range(5):
    print(i)
print("list(range(5, 10))")
print(list(range(5, 10)))
print("list(range(0, 10, 3))")
print(list(range(0, 10, 3)))
print("list(range(-10, -100, -30))")
print(list(range(-10, -100, -30)))

  

#Para iterar sobre os índices de uma sequência, combine range() e len() da seguinte forma:

a = ['Mary', 'had', 'a', 'little', 'lamb']
for i in range(len(a)):
    print(i, a[i])

  
  
#Um laço for ou while pode incluir uma cláusula else.
#comando break sai do laço.

for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'equals', x, '*', n//x)
            break
	    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')


#A instrução continue, também emprestada da linguagem C,
# continua com a próxima iteração do laço:

for num in range(2, 10):
    if num % 2 == 0:
        print("Found an even number", num)
        continue
    print("Found an odd number", num)

  
#O comando pass não faz nada.
# Pode ser usada quando a sintaxe exige um comando mas a semântica do programa não requer nenhuma ação.
```
 

