Sintaxe

Classes são as "receitas" de construção dos "objetos".
Mas o que são objetos? 

Objeto, de forma simples e direta é uma estrutura computacional que possui atributos e métodos?
Mas que raio de explicação é essa?

Primeiro vamos entender uma Classe.

Uma classe pode conter apenas atributos, assim sendo apenas uma estrutura que guarda dados.
Uma classe pode ter apenas métodos, sendo assim um tipo de "biblioteca".
Uma classe pode ter os dois, atributos e funções constituindo assim uma receita para criar objetos.

O que são esses "Atributos"? 
Os atributos são variáveis ou constantes que são declarados na construção da classe.
Cada vez que uma classe é "instanciada" (significa que se criou uma estrutura a partir da classe enquanto a programação é executada) os atributos são como variáveis e podem receber diversos valores.

O que são os métodos?
Métodos são funções que pertencem à classe. 
São funções que são definidas dentro do objeto.

Então, segue um exemplo pra tentar deixar mais claro.

```python
class Pessoa:

    def __init__(self, nome, idade, sexo, profissao):
        self.nome = nome
        self.idade = idade
        self.sexo = sexo
        self.profissao = profissao
  

    def altera_profissao(self, nova_profissao):
        self.profissao = nova_profissao


pessoa1 = Pessoa("Mateus", 42, "M", "")
pessoa2 = Pessoa("Luiza", 41, "F", "Perita Criminal")
  
print("Nome pes. 1: ",pessoa1.nome)
print("Nome pes. 2: ",pessoa2.nome)
print("Idade pes. 1: ",pessoa1.idade)
print("Idade pes. 2: ",pessoa2.idade)
print("Sexo pes. 1: ",pessoa1.sexo)
print("Sexo pes. 2: ",pessoa2.sexo)
print("Profissao pes. 1: ",pessoa1.profissao)
print("Profissao pes. 2: ",pessoa2.profissao)

  

pessoa1.altera_profissao("Programador")

print("Nome pes. 1: ",pessoa1.nome)
print("Idade pes. 1: ",pessoa1.idade)
print("Sexo pes. 1: ",pessoa1.sexo)
print("Profissao pes. 1: ",pessoa1.profissao)
```


Explicando o código acima temos:

class - palavra reservada que define uma classe.

def - é a palavra reservada que define uma função.

 _ _ init(argumentos) _ _ -  isso define o "construtor" do objeto. Quando o processador cria a estrutura na hora em que o programa está rodando essa definição _ _ init() _ _ é o que ele entende que deve chamar para construir o objeto.
 Note que ele PODE receber valores/argumentos para inicializar os atributos do objeto.
 
 Temos então alguns atributos:  nome, idade, sexo, profissao;
 
 A palavra "self" indica que os valores que serão aplicados aos atributos pertencem ao objeto criado através do chamado daquele _ _ init() _ _ . 
 O "self" representa a própria instancia que é criada na hora da execução.
 
 Quando aplicamos um valor com
  ```python 
 self.nome = nome
 ```
Estamos colocando o valor que vem em "nome" no atributo nome do objeto criado.

Quando não usamos o _ _ init() _ _  e usamos apenas o "def", estamos criando um método da classe. Isso é, uma função que faz parte do objeto criado.

Ainda no código acima temos 
```python
pessoa1 = Pessoa("Mateus", 42, "M", "")
pessoa2 = Pessoa("Luiza", 41, "F", "Perita Criminal")
```

É nesse momento que o programa cria o "objeto" pessoa e aplica os valores "Mateus", 42, "M" "" e "Luiza", 41, "F", "Perita Criminal" a duas estruturas diferentes (pessoa1 e pessoa2) criadas a partir da mesma receita (class Pessoa).

A partir daí é possível acessar os atributos e executar os métodos do objeto criado a partir do nome do objeto e ".", por exemplo:

```python
print("Nome pes. 1: ",pessoa1.nome)
```
Aqui o sistema vai imprimir o valor que está guardado no objeto pessoa1 no atributo nome.

```python
pessoa1.altera_profissao("Programador")
```
Aqui o sistema vai usar o método "altera_profissao()" do objeto pessoa1 para trocar o valor do atributo profissao.

[[Atributos privados]]
