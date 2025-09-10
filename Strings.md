Sintaxe

Strings são basicamente texto. Normalmente são alocadas/guardadas em variáveis, mas podem ser manipuladas diretamente também.

Existem duas maneiras de definir uma string:

1- Entre aspas duplas "isto é uma string"
2- Entre aspas simples 'isto é outra string'

Importante: Quando criamos uma string, cada caractere tem um numero/índice associado, por exemplo:

```python
var_string_1 = "Uma String"
```


 Cada caractere de "Uma String" tem um numero associado começando do 0.
 U - 0
 m - 1
 a - 2
(espaço) - 3 
 S - 4
 t - 5
 r - 6
 i - 7
 n - 8
 g - 9

Isso permite manipular a String.
A String é considerada um "Objeto" e tem suas próprias funções à disposição para que seja manipulada.

```python
#Strings

import string

varStr1 = 'Esta é a string de teste 1.'
varStr2 = "Esta é a string de teste 2."
varStr3 = "\n"

  

print("Strings: ")
print("varStr1: "+varStr1)
print("varStr2: "+varStr2)
print("O próximo deve pular uma linha.")
print(varStr3)


#Concatenacao

print("Concatenação -> Esta é uma string : + varStr1")
print("Esta é uma string : "+varStr1)
print("")


#Interpolacao
print('Interpolacao -> tamnho de varStr1 => %d' %len(varStr1))
print("")


#Sequencia
print("Sequencia de varStr1: ")
for ch in varStr1: print(ch)
print("")

  

#Objeto
print("Strings são objetos: ")
if varStr1.startswith('E'): print(varStr1)
print("")

  
#Repetição
print("Repetir a String varStr2 3 vezes: ")
print(3*varStr2)
print("")

  
#Função format()
musicos = [('Page', 'guitarrista', 'Led Zeppelin'),
           ('Bruce D.', 'vocalista', 'Iron Maiden')]


#variável com  formatação
msg = '{0} é {1} de {2}'
for nome, funcao, banda in musicos:
    print(msg.format(nome, funcao, banda))
print("")    


#Fatias de Strings
print("Fatiando a varStr2:")
print("varStr2 -> "+varStr2)
print("varStr2[0] -> "+varStr2[0])
print("varStr2[3:] -> "+varStr2[3:])
print("varStr2[:3] -> "+varStr2[:3])
print("varStr2[:-2] -> "+varStr2[:-2])
print("")

  
#Invertendo uma String
print("Invertendo a varStr2:")
print("varStr2 -> "+varStr2)
print("varStr2[::-1]")
print(varStr2[::-1])
print("")

  

#Funções uteis de strings
varStr4 = "Esta é a string de teste 4."
varStr5 = " Esta é a string de teste 5. "

print("Mais Strings: ")
print("varStr4: "+varStr4)
print("varStr5: "+varStr5)
print("\n")

  
#Replace
varStr6 = varStr4.replace('Esta é a string', 'Texto')
print("Trocando uma parte da string")
print("varStr6 = varStr4.replace('Esta é a string', 'Texto')")
print("varStr6: "+varStr6)
print()

  
#Find
print("Retorna o PRIMEIRO indice da letra procurada:")
indiceFind = varStr6.find('x')
print("varStr4.find('s'): ",str(indiceFind))
print()

  
#Strip
#Remove os espaços da string
print("varStr5.strip() - remove espaços antes e no fim da String")
print(varStr5.strip())
print()
```
