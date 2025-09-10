Sintaxe

Variáveis são espaços em memória que o sistema cria conforme a programação (fonte) para guardar informações (dados, valores, etc.).

Em outras linguagens mais antigas era necessário definir o tipo de variável quando a mesma era declarada. 

Em Python a tipagem é dinâmica e muitas vezes dita como "fraca", ou seja, não é necessário definir um tipo de variável quando se declara a própria variável.

Durante a execução do programa ou até mesmo durante a sua compilação, o tipo de uma variável poderá ser alterado.


REGRAS:

A variável deve ser nomeada em letras minúsculas e caso tenha espaços no nome, estes devem ser substituídos por "__".

Ex:

```python
esta_e_uma_variavel = "aqui vao dados"
```



NOTA:

O símbolo "=" serve para atribuir/aplicar o valor à variável.
Em outros casos, quando vamos comparar variáveis usamos o 
```python
 == 
```
para comparar valores. ENTAO CUIDADO!


No entanto nem tudo pode ser guardado em variáveis.
Temos alguns tipos de dados que as variáveis aceitam e podemos forçar :

INTEIRO:
Numero inteiro
```python
inteiro = 15
print(type(inteiro)) # <class 'int'>
```

Declaramos uma variável de nome 'inteiro' e colocamos o valor 15 nela.
Quando usamos print(type(inteiro)) vemos na tela qual o tipo de variável o sistema criou para receber o valor 15. (Seria como se o tipo da variável fosse definido conforme o valor que é colocado nela).

FLOAT:
Numero decimal, com partes decimais.
```python
ponto_flutuante =  25.10
print(type(ponto_flutuante)) # <class 'float'>
```

STRING:
Texto
```python
nome = "Treinaweb"
print(type(nome)) # <class 'str'>
```

BOOLEAN:
Verdadeiro ou Falso (Ligado ou Desligado)
```python
booleano = True
print(type(booleano)) # <class 'bool'>
```

COMPLEXO:
Representação de números complexos.
```python
complexo = 25 + 3j
print(type(complexo)) # <class 'complex'>
```



