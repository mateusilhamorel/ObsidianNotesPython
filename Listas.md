Sintaxe

Listas são conjuntos de dados/informações que guardamos em uma variável.
Os elementos das listas são indexados por números inteiros.
Os elementos das listas são MUTÁVEIS.

```python
#Listas

#Sintaxe lista = [a, b, ..., z]

progs = ['Iron Maiden', 'Black Sabbath', 'Metallica', 'Megadeath', 'Helloween', 'Rob Zombie']


#Varrer Lista
print("varrer lista com for: ")
for band in progs: print(band)
print("")
print("")

  
#Trocar o ultimo elemento:
print("Trocar o ultimo elemento: ")
progs[-1] = 'Type O Negative'
for band in progs: print(band)
print("")
print("")

  
#Incluir elemento:
print("Incluindo elemento: ")
progs.append("Rob Zombie")
for band in progs: print(band)
print("")
print("")

  
#Remover elemento
print("Remover elemento: ")
progs.remove("Type O Negative")
for band in progs: print(band)
print("")
print("")

  
#Ordenar a lista
print("Ordenar a lista: ")
progs.sort()
for band in progs: print(band)
print("")
print("")

  

#Inverter a lista
print("Inverter a lista: ")
progs.reverse()
for band in progs: print(band)
print("")
print("")

  
#Pegar item especifico da lista:

print("Pegar item especifico da lista: ")
print("Item 3 da lista atual: "+progs[3])
print("")
print("")

  
#Pegar o indice de um elemento da lista
print("Pegar indice do -Helloween- na lista atual: ")
print("Indice do Helloween da lista atual: "+ str(progs.index('Helloween')))
print("")
print("")

  
#Unindo listas:
pops = ['Elvis', 'Coldplay', 'Michael Jackson', 'Gorillaz']
print("Lista progs")
print(progs)
print("Lista pops")
print(pops)

listaUnificada = progs+pops
print("Lista listaUnificada")
print(listaUnificada)
print("")

print("")
```

