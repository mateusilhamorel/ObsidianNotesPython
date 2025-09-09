Sintaxe

Operadores são sinais que executam alguma operação entre DUAS ou MAIS informações.
O que conhecemos mais são os operadores ARITMETICOS da matemática, mas estes não são os únicos....

O mais comum é usarmos operadores entre variáveis ou entre uma variável e um valor.

OPERADORES ARITMETICOS:

```python
#variaveis

varFloat1 = 56.78
varFloat2 = 23.45
varInt1 = 3
varInt2 = 7

print("Float 1: "+str(varFloat1))
print("Float 2: "+str(varFloat2))
print("Float 1: "+str(varInt1))
print("Float 1: "+str(varInt2))
print("")

  

#Soma

print("Soma float 1 + float 2")
print(varFloat1+varFloat2)
print("Soma int 1 + int 2")
print(varInt1+varInt2)
print("Float 1 + Int 2")
print(varFloat1+varInt2)
print("")


#Diferença

print("Diferença float 1 - float 2")
print(varFloat1-varFloat2)
print("Diferença int 1 - int 2")
print(varInt1-varInt2)
print("Float 2 - Int 2")
print(varFloat2-varInt2)  
print("")


#Multiplicacao

print("4 x Float 2")
print(4*varFloat2)
print("Int 1 x 8")
print(varInt1*8)  
print("Int 1 x Float 1")
print(varInt1*varFloat1)
print("")


#Divisao (resultado real)

print("Divisao real entre Int 2 por Int 1")
print(varInt2/varInt1)
print("Divisao real entre Float 1 por Float 2")
print(varFloat1/varFloat2)  
print("")


#Divisao (resultado inteiro)

print("Divisao inteira entre Int 2 por Int 1")
print(varInt2//varInt1)
print("Divisao inteira entre Float 1 por Float 2")
print(varFloat1//varFloat2)
print("")


#Modulo

print("Modulo: retorna o resto da divisao")
print("Float 1 por Float 2")
print(varFloat1%varFloat2)
print("")


#Potencia

print("Potenciação")
print("2 elevado a 3")
print(2**3)
```



OPERADORES LOGICOS:

```python
#Variáveis

varF1 = 35.67
varF2 = 17.21
varI1= 8
varI2= 3
varT = True
varF = False
varB1 = 11 #inteiro para ser mostrado como binario
varB2 = 5 #inteiro para ser mostrado como binario

print("Float 1: "+str(varF1))
print("Float 2: "+str(varF1))
print("Inteiro 1: "+str(varI1))
print("Inteiro 2: "+str(varI2))
print("Var true: "+str(varT))
print("Var false: "+str(varF))
print("Binario 1: "+bin(varB1))
print("Binario 2: "+bin(varB2))
print("")

  
#Operaçoes lógicas

print("Menor \">\"   Float 1 é menor que Float 2?")
print(varF1>varF2)
print("Maior \"<\"   Float 1 é maior que Float 2?")
print(varF1>varF2)
print("Menor ou igual \"<=\"   Float 1 é menor que Float 2?")
print(varF1<=varF2)
print("Maior ou igual \">=\"   Float 1 é maior que Float 2?")
print(varF1>=varF2)
print("Igual \"==\"   Float 1 é igual a Float 2?")
print(varF1==varF2)
print("Diferente \"!=\"   Float 1 é diferente de Float 2?")
print(varF1!=varF2)
print("")

  

#OPeracoes bit a bit

print("Deslocamento para esquerda <<")
print("Binario antes: "+bin(varB1))
print("Binario depois: "+bin(varB1<<1))
print("Deslocamento para direita >>")  
print("Binario antes: "+bin(varB1))
print("Binario depois: "+bin(varB1>>1))
print("Operação E entre dois binarios B1 E B2")
print(bin(varB1&varB2))
print("Operação OU entre dois binarios B1 e B2")
print(bin(varB1|varB2))
print("Operação OU exclusivo entre dois binarios B1 e B2")
print(bin(varB1^varB2))
print("Inversão de um binario B1")
print(bin(~varB1))
print()

  
  
#Logicos

print("AND logico entre varT e varF")
print("varT and varF")
print(varT and varF)
print("varT & varF")
print(varT and varF)
print()


print("OR logico entre varT e varF")
print("varT or varF")
print(varT or varF)
print("varT | varF")
print(varT | varF)
print()


print("NOT logico do varT ")
print("not varT")
print(not varT)
print()

print("2 in (2, 3)")
print(2 in (2, 3))
print("")

print("2 is 3")
print(2 is 3)
print("")


```



OPERADOR TERNARIO:
É o único operador que trabalha com 3 informações:
Ele avalia uma condição. Dependendo da condição (verdadeira ou falsa) ele retorna um ou outro valor.

```python
lockdown = True
status = 'Em casa.' if lockdown else 'Liberado.'

print(status)
```


ALGUMAS FUNÇÕES ESPECIAIS:

```python
#variaveis

varF1 = -76.89
varI1 = 6
varI2 = 3


print("varF1: "+str(varF1))
print("varI1: "+str(varI1))
print("varI2: "+str(varI2))
print("")


print("Funcao abs() retorna o valor absoluto, por exemplo abs(varF1)")
print(abs(varF1))
print("Conversão para base dois binario - apenas para impressão - bin(varI1)")
print(bin(varI1))
print("Conversão para base octal - apenas para impressão - oct(varI1)")
print(oct(varI1))
print("Conversão para base hexa - apenas para impressão - hex(varI1)")
print(hex(varI1))
print("Potenciação pow(3,4)")
print(pow(3,4))
print("Arredondamento round(varF1,1)")
print(round(varF1,1))
```


OPERADORES BOOLEANOS
 
