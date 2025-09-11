Sintaxe

A melhor definição de DICIONARIO que consegui pensar é que é uma lista onde é possível definir o índice.

Se você ainda não viu Lista, procure aqui [[Listas]].

O dicionário é um conjunto de CHAVE-VALOR (como as listas hash).
O VALOR É MUTÁVEL.
A CHAVE DEVE SER IMUTÁVEL.
A CHAVE NÃO PODE SER REPETIDA (Porque vai trabalhar no lugar do índice, e não podemos ter dois índices iguais).

```python
#Bandas e seus albuns
bands = {'Metallica':['Black', 'Load', 'Reload'],
         'Iron Maiden':['Iron Maiden', 'Powerslave', 'Piece of Mind'],
         'Ozzy':['Diary o a madman', 'Black Rain', 'Bark at the moon']
         }

  

#Mais bandas
bands['Linking Park'] = ['Hybrid Theory', 'Meteora']
  
#itens() retorna uma lista de tuplas com a chave e o valor
for band, albuns in bands.items():
    print(band, '=>', albuns)
print("")

  

#Quantidade de itens
print(len(bands), 'bandas')
print("Apaga par Chave:Valor usando del(bands)['Ozzy']")
del(bands)['Ozzy']
for band, albuns in bands.items():
    print(band, '=>', albuns)
print("")

  
print(bands.items())
  
bands2={'Ozzy':['Diary o a madman', 'Black Rain', 'Bark at the moon'],
        'Helloween' : ['Keeper of Keys', 'Better Than Raw', 'The dark ride']}
print(bands2.items())

print("")
print("")
print("")

bands.update(bands2)
for band, albuns in bands.items():
    print(band, '=>', albuns)
print("")
```




