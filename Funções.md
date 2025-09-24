Sintaxe

Uma função é um modo de definir um conjunto de comandos que vai realizar um processamento/tarefa. Esse conjunto de dados pode ser reutilizado. É possível criar [[Pacotes]] que podem ser usados em diferentes partes do projeto/sistema.

Por exemplo: Sistema de controle monetário com calculo de juros.

Em um sistema financeiro, diversas rotinas usam o cálculo de juros em diversas rotinas.
Não é uma boa ideia implementar o cálculo em cada uma das rotinas de forma isolada.
Porque? Porque sempre que existir uma modificação ou uma manutenção será necessário alterar TODAS as rotinas que usam o cálculo.

Então é uma ótima ideia fazer esse cálculo em um lugar só e usar essa rotina de cálculo em todos os pontos necessários.

Como funciona uma função? 

Uma função PODE OU NÃO receber dados para processar.
A função executa o que está programado.
A função PODE retornar alguma coisa.
A função pode conter [[Docstrings]]
A função DEVE possuir um NOME.

Definindo uma função:



def nome_da_função (parâmetros):
		""""docstrings"""
		comandos
		return



def - palavra reservada do python que serve para definir uma função.
nome_da_função - é o nome que você vai dar para a função e vai usar quando for chamar a função.
() - aqui define se vai receber parâmetros e/ou quantos parâmetros a função vai receber.
:  - a partir daqui começam os comandos que vão compor a rotina.
"""docstrings""" -  o que estiver dentro de """ """ é um descritivo formal do que a função faz
comandos - define os comandos da função (o que ela deve fazer)
return - retorna algum valor (opcional).


IMPORTANTE:

Em Python a escrita/codificação é meio "solta", no sentido de não ter caracteres definindo onde começa e onde termina a função. 

O que define o que está dentro do corpo da função é o espaçamento/identação que ela tem, ou seja, os comandos do corpo da função deve estar espaçados de forma a ficar deslocados da linha da função. Observe os espaçamentos abaixo no exemplo. 



Exemplo: 

```python
def faz_uma_soma(n1, n2):
	"""Esta função faz uma soma"""
	 n3 = n1+n2
	 return n3
```



Agora, sempre que você quiser chamar a função NO MESMO FONTE, basta digitar faz_uma_soma  e colocar os valores a serem somados no lugar de n1 e n2 (n1, n2). O ideal é armazenar isso em uma terceira variável como exemplo abaixo:

```python
def faz_uma_soma(n1, n2):
	"""Esta função faz uma soma"""
	 n3 = n1+n2
	 return n3
	 
	 
valor = faz_uma_soma(544, 234)
print("Valor da soma: "+valor)
```





PARAMETRO PADRAO:

Podemos definir na função um parâmetro padrão, ou seja, um valor que seja aplicado caso a função seja chamada sem parâmetro nenhum.

Exemplo: 

```python
def padrao(valor=100):
    """Função que apenas imprime um valor"""
    print("O valor definido foi: " + str(valor))
padrao() # 100
padrao(10) # 10
padrao(33) # 33
```




NAMESPACES e ESCOPO

NAMESPACE é um conceito abstrato um pouco difícil de entender no início. É quase o que o próprio nome diz NAMESPACE (espaço de nomes). 

Vou tentar explicar o conceito: 

Imagine que quando você inicia o interpretador python você entre em uma "caixa" (que representa o espaço onde você vai criar e executar suas tarefas). Neste espaço existem nomes pré-definidos que podem e são usados pelo python. 

```python
dir(__builtins__)
[
    'ArithmeticError',
    'AssertionError',
    'AttributeError',
    'BaseException',
    ...
    'super',
    'tuple',
    'type',
    'vars',
    'zip'
]
```

Em sua maioria (talvez totalidade) são funções internas.

Agora, digamos que você crie um fonte python para fazer alguma coisa, um módulo. Esse módulo terá seu próprio nome de espaço. As variáveis e funções serão criadas dentro deste espaço. Esse espaço é chamado de espaço global.

E finalmente no seu fonte você cria uma função. A função também tem seu próprio espaço onde coisas são definidas. Esse espaço é chamado de espaço local.

Daí vem o "Escopo".

Cada vez que você chama uma função o python cria um espaço novo (em memória) e as variáveis de uma chamada de função serão distintas de outra chamada de função, mesmo que a função chamada seja a mesma.

Então existe uma sequência para que o python procure uma informação:

1. **Local** : O Python procura `x`dentro da função interna. Se não encontrar `x`, move-se para o escopo envolvente.
2. **Enclausurando** : Em seguida, o Python procura `x`no escopo da função envolvente. Se não for encontrado lá, ele move para o escopo global.
3. **Global** : O Python procura `x`no escopo global. Se ainda assim não encontrar, ele move para o escopo interno.
4. **Integrado** : Por fim, o Python procura `x`no escopo integrado. Se não encontrar `x`, gera uma exceção "NameError".
   
Consulte os erros em [[Erros]].   




ARGUMENTOS VARIÁVEIS

Podemos passar um numero variável de argumentos para uma função usando * args 
Exemplo: 

```python
def soma(*args):
    total = 0
    for num in args:
        total += num 
    return total

print(soma(2,3,4,6)) # 15
print(soma(2,3,4,6,5,5,5,1,2)) # 32
print(soma(2,3)) # 5
```

Podemos usar palavra-chave como argumento usando ** kwargs
Exemplo:

```python
def pessoa(**kwargs):
    print(kwargs)
    for nome, idade in kwargs.items():
        print(f'{nome} tem atualmente {idade} anos de idade')
pessoa(gabriel='33', rafael='47', daniel='22')

# {'gabriel': '33', 'rafael': '47', 'daniel': '22'}
# gabriel tem atualmente 33 anos de idade
# rafael tem atualmente 47 anos de idade
# daniel tem atualmente 22 anos de idade
```

 
 
 RECURSAO

A forma mais fácil de entender recursão é pensar que uma função chama ela mesma dentro dela.
Isso é PERIGOSO caso não seja feito com cuidado, porque exige a definição de um critério de parada, para parar de chamar a função em algum momento. Se esse critério tiver alguma falha, a função pode ficar chamando ela mesma eternamente até acabar com a memória do sistema (loop infinito).

Exemplo:

```python
def fatorial(x):
    """
    Essa é uma função recursiva
    Ela calcula o fatorial de um número inteiro
    """
    if x == 1:
        return 1
    else:
        return (x * fatorial(x - 1))
y = 4
z = 10

print("O fatorial de {0} é {1}".format(y,fatorial(y))) # O fatorial de 4 é 24
print("O fatorial de {0} é {1}".format(z,fatorial(z))) # O fatorial de 7 é 3628800
```

Observe que no caso acima o critério de parada é quando x = 1 pois não vai mais chamar a própria função, e isso interrompe a cadeia. Observe o que acontece com o valor 4 por exemplo:

Chamamos a função fatorial com o parâmetro 4
Ela verifica que não é 1 e chama a função com valor 4-1 para multiplicar com 4.
Aí a função foi chamada com valor 3 (calculado acima) e chama novamente com o valor 3-1.
Chama novamente com o valor 2, mais uma vez não é o valor 1 então chama novamente com 2-1.
Agora sim, ela retorna com 1 e vai executando as multiplicações anteriores até chegar na função inicial que disparou o processo.

```python
fatorial(4)              # Primeira chamada com 4
4 * fatorial(3)          # Segunda chamada com 3
4 * 3 * fatorial(2)      # Terceira chamada com 2
4 * 3 * 2 * fatorial(1)  # Quarta chamada com 1
4 * 3 * 2 * 1            # Retorno da quarta chamada, uma vez que y = 1
4 * 3 * 2                # Retorno da terceira chamada
4 * 6                    # Retorno da segunda chamada
24                       # Retorno da primeira chamada
```

Usando a analogia do NAMESPACE, é como se fosse uma boneca Matrioshka, que vai criando um espaço dentro do outro

Consulte [[Exceções]] para evitar travamentos de execução.
Consulte [[Traceback]] para entender as calls de função.
Consulte [[Funções especiais]] para conferir algumas funções especiais.