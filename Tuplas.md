Sintaxe

Tuplas são conjuntos.
Armazena-se em uma variável um conjunto de valores ou dados.
São como listas. Porém as tuplas não são modificáveis.

```python
#Tuplas
tupla = (1, 2, 3, 4, 5)
print("tupla -> "+str(tupla))

#Pelo indice
print("item 2 da tupla -> "+str(tupla[2]))

#Desempacotando uma tupla:
a, b, c, d, e = tupla

print(a)
print(b)
print(c)
print(d)
print(e)
print("")
```