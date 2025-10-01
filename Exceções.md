Sintaxe

Existe uma estrutura em Python (assim como em outras linguagens de programação) que permite que o programa siga executando mesmo que ocorra um erro ou uma condição de exceção.

Essa estrutura é o Try - Except - Finally.

Como isso funciona? 


Envolvemos um bloco de comando dentro de um try e se houver algum erro, ao invés de travar a execução o sistema emite um "aviso de exceção" que é processado pelo bloco except. 

Existem diversos erros que são captados pelo try-except:

- **Erros de Sintaxe**: 
    
    Ocorrem quando o código é escrito de forma que o interpretador não consegue analisar. 
    
    - `SyntaxError`: Indica um erro de sintaxe na linguagem Python. 
    - `IndentationError`: Ocorre quando há um recuo (indentação) incorreto no código.

- **Erros de Execução**: 
    
    Causados por operações que não são válidas ou que não podem ser executadas. 
    
    - `ZeroDivisionError`: Surge ao tentar dividir um número por zero. 
    - `TypeError`: Ocorre quando uma operação ou função é aplicada a um objeto de tipo inadequado. 
    - `NameError`: Gerada quando um nome (variável, função, etc.) não é encontrado no escopo atual. 
    - `ValueError`: Ocorre quando um argumento tem o tipo correto, mas um valor inapropriado. 
    - `IndexError`: Levantada quando um índice de sequência (como uma lista) está fora do intervalo válido. 
    - `AttributeError`: Ocorre quando se tenta acessar ou atribuir um atributo inexistente a um objeto.

- **Erros de Entrada e Saída (I/O)**: 
    
    Relacionados a operações de manipulação de arquivos e entrada/saída. 
    
    - `FileNotFoundError`: Levantada quando se tenta abrir um arquivo que não existe. 
    - `OSError`: Uma categoria mais ampla para erros relacionados ao sistema operacional.


- **Outras Exceções Comuns** 
    - `ImportError`: Gerada quando a importação de um módulo falha. 
    - `KeyboardInterrupt`: Capturada quando o usuário interrompe a execução com `Ctrl+C`. 
    - `AssertionError`: Levantada quando uma instrução `assert` falha. 
    - `MemoryError`: Ocorre quando não há memória suficiente para alocar um objeto. 
    - `RuntimeError`: Uma exceção genérica para erros não cobertos por outras categorias.


Um Exemplo básico:

```python
try:
    a = int(input('Numerador: '))
    b = int(input('Denominador: '))
    r = a / b
except ZeroDivisionError:
    print('Erro ao dividir por zero.')
```

É possível usar um except genérico para pegar qualquer erro, mas isso esconde problemas de execução:

```python
try:  
# Code that might raise an exception  
result = 10 / 0  
except:  
print("An error occurred.")
```

Você pode aplicar múltiplos excepts para tentar obter os erros específicos:

```python
try:  
	value = int("abc")  
except ValueError:  
	print("Invalid input: Please enter a number.")  
except ZeroDivisionError:  
	print("Cannot divide by zero.")
```

Usando o "else" no try:

O bloco do else só é executado SE o try não gerar nenhum erro:

```python
	try: 
		x = int(input("Digite um número: ")) 
		y = int(input("Digite outro número: ")) 
		resultado = x / y 
	except ZeroDivisionError: 
		print("Erro: Não é possível dividir por zero!")
	except ValueError: 
		print("Erro: Entrada inválida! Por favor, digite um número.") 
	else: 
		print(f"O resultado é: {resultado}")
```

Usando o Finally:
O bloco finally é executado independentemente de qualquer exceção que ocorra. Isso é útil para liberar recursos ou executar ações de limpeza.

```python
try: 
	x = int(input("Digite um número: ")) 
	y = int(input("Digite outro número: ")) 
	resultado = x / y 
except ZeroDivisionError: 
	print("Erro: Não é possível dividir por zero!") 
except ValueError: 
	print("Erro: Entrada inválida! Por favor, digite um número.") 
else: 
	print(f"O resultado é: {resultado}") 
finally: 
	print("Execução finalizada.")
```


Raise:

Raise é uma palavra reservada do python que faz com que o erro seja tratado imediatamente evitando que o erro se propague pela execução.

Além de usar exceções embutidas, podemos criar nossas próprias exceções personalizadas. Isso é útil quando queremos fornecer mensagens de erro mais específicas ou quando estamos desenvolvendo uma biblioteca e queremos que os usuários lidem com erros de maneira específica.


Para isso é necessário criar uma classe :

```python
class DivisaoPorZeroError(Exception):
    def __init__(self, mensagem):
        self.mensagem = mensagem
        super().__init__(self.mensagem)

def dividir(a, b):
    if b == 0:
        raise DivisaoPorZeroError("Não é possível dividir por zero!")
    return a / b

try:
    resultado = dividir(10, 0)
except DivisaoPorZeroError as e:
    print(f"Erro: {e.mensagem}")
```

