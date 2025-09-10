O if (do inglês "se") é uma estrutura que permite uma tomada de decisão ao se avaliar uma "condição".

Se (calor hoje E dinheiro no bolso) - então tomar sorvete.
Caso contrário - ficar em casa e passar calor.

Essa estrutura de decisão pode ser construída em python da seguinte maneira:

```python
#Variáveis para avaliação da situação
calor = true
dinheiro = true

if calor and dinheiro :
	print('Tomar sorvete')
else
    print('Ficar em casa passando calor')    	

``` 

IMPORTANTE: 
Em outras linguagens existem delimitadores para marcar onde começa e onde termina a estrutura, por exemplo no JAVA:

```java
boolean calor = true;
boolean dinheiro = true;
if(calor && dinheiro){
	System.println("Tomar sorvete");
}else{
	System.println("Ficar em casa passando calor");
}
```

Observe que no caso do Java o if tem "()" para definir o que ele vai avaliar para tomar a decisão.
Também tem os "{}" que definem o corpo de instruções que serão executados em cada caso.

NO PYTHON ISSO É DEFINIDO PELA "IDENTACAO", ou seja, pela estrutura gráfica do que é escrito.

O if no python avalia tudo que estiver entre o if e ":" 
Caso verdadeiro ele vai executar a instrução que estiver abaixo dele indentada com um espaçamento (esse espaçamento horizontal que "desalinha" o comando de baixo é muito importante).

Podemos usar o IF sozinho, sem o "else", caso seja uma decisão simples:

```python
if calor and dinheiro :
	print('Tomar sorvete')
```

No caso acima não temos a instrução caso a avaliação seja falsa.


ANINHAMENTO DE SELEÇÕES

Podemos fazer um aninhamento de IFs para casos onde existam mais de uma opção a tomar com base em diversas avaliações (nesses casos ao invés do "else" usamos "elif" que é uma contração de else + if):

```python
x = 0

if x < 0:
    x = 0
    print('Negative changed to zero')
elif x == 0:
    print('Zero')
elif x == 1:
    print('Single')
else:
    print('More')
```

