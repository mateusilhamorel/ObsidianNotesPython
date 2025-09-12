Sintaxe


Pacotes também são comumente chamados de Módulos em Python. Para ser honesto é mais comum encontrar o nome Módulo, do que pacotes, mas pode se dizer que são a mesma coisa.

**Módulo** é um arquivo que contém definições e comandos/instruções **Python**.

Um módulo/pacote é comumente visto como uma biblioteca, ou melhor, uma caixa de ferramentas.

Então quando importamos um módulo em nosso arquivo fonte, as ferramentas/funções que o módulo oferece ficam disponíveis para uso.

Vamos começar esse estudo com módulos pré-prontos, ou seja, um módulo que você importa de fora do seu sistema (instala - faça em um ambiente virtual para não poluir a instalação do python original).

Vamos ver o processo em uma sequência e entender o que estamos fazendo e porque.....

Primeiro defina em seu computador uma pasta onde irá trabalhar com os fontes. 
Eu escolhi : 

D:\PY\PYTHON_BASE\

Em um terminal ou no seu ambiente de desenvolvimento (já configurado) crie um ambiente virtual de nome MATEMATICA:

```python
D:\PY\PYTHON_BASE> python -m venv MATEMATICA
```

Note que vai ser criada uma nova pasta com o nome MATEMATICA dentro da pasta corrente.

Agora, para ativar o ambiente use: 
```python
D:\PY\PYTHON_BASE> MATEMATICA\Scripts\activate
```

Magicamente o seu ambiente virtual vai ficar ativo:
```python
(MATEMATICA) PS D:\PY\PYTHON_BASE>
```

O (MATEMATICA) indica que o ambiente virtual está ativo.

Agora, vamos instalar neste ambiente um pacote externo por meio do [[Pip]].
Escolhi o NumPy que é uma biblioteca de matemática.

Execute: 
```python
(MATEMATICA) PS D:\PY\PYTHON_BASE> pip install numpy
```

O sistema vai instalar os pacotes necessários para a utilização da biblioteca/modulo numpy
Você poderá verificar algumas pastas foram adicionadas à pasta MATEMATICA.

Agora, crie um arquivo fonte Calculos.py na pasta MATEMATICA.

Neste arquivo, vamos importar o numpy através de :

```python
import numpy as np
```

Isso vai permitir usar as funções de numpy no meu fonte.
Como exemplo vamos criar uma matriz:

```python
import numpy as np

print(np.__version__)
matriz = np.array([[2, 3, 1], [4, 5, 7]])
print(matriz)
```

Ao rodar esse fonte vamos receber:

```python
(MATEMATICA) PS D:\PY\PYTHON_BASE\MATEMATICA> python Calculo.py
2.3.3
[[2 3 1]
 [4 5 7]]
```

A primeira linha impressa é a versão da biblioteca importada.
As duas demais são uma impressão da matriz montada com a função array.


Então, acima fizemos um exemplo onde importamos um pacote/módulo pronto. É uma biblioteca externa que podemos usar no projeto.

FECHE O AMBIENTE VIRTUAL:

```python
(MATEMATICA) PS D:\PY\PYTHON_BASE\MATEMATICA> deactivate
```




MONTANDO UM PACOTE/MÓDULO

Você pode montar seus próprios módulos para usar em seus projetos.
É relativamente simples.

Escolha uma pasta para trabalhar com esses fontes.
NESSE CASO NÃO PRECISA CRIAR UM AMBIENTE VIRTUAL (nada será instalado).

```python
D:\PY\PYTHON_BASE\Estudo\Modulos>
```

Dentro desta pasta crie outra pasta nomeada Matematico e dentro dela o fonte:
Matematico.py

```python
#Modulo Exemplo Funcoes matematicas

def eq2gRoots(a: int, b: int, c: int):
    """Retorna raizes para equacao de segundo grau"""
    if a == 0: #Reta
        return -c/b
    else:
        d = (b**2 -4*a*c)**0.5
        x1 = (-b - d)/(2*a)
        x2 = (-b + d)/(2*a)
        return x1, x2
        
def soma(x: int, y: int):
    """Retorna a soma de dois numeros"""
    return x + y        
```

Quando finalizar, acesse a pasta onde se encontra o arquivo Matematico.py e rode o seguinte comando:

```python
PS D:\PY\PYTHON_BASE\Estudo\Modulos\Matematico> python -m py_compile Matematico.py
```
Isso vai gerar uma compilação do fonte e vai possibilitar importar funções separadamente.


Na  pasta anterior : 
```python
PS D:\PY\PYTHON_BASE\Estudo\Modulos> 
```
Crie outro fonte nomeado: 
Calc.py

```python
def media(lista):
    return float(sum(lista))/len(lista)
```


E agora, finalmente o arquivo que vai usar os dois acima: 
Run.py

```python
#Importa da mesma pasta
#Importa da mesma pasta

import Calc
from Matematico import Matematico as mat

##Usa rotinas do modulo importado
l=[23, 54, 31, 77, 12, 34]

  
#chama a rotina importada
print("Media da lista: "+str(Calc.media(l)))


#Import do modulo matematico em outra pasta
print(mat.eq2gRoots(0, 2, -2))
```

Observe o seguinte: 
Importamos totalmente o fonte Calc.
Mas importamos  de outra pasta o fonte Matematico com o nome de mat (observe onde usa a função mat.eq2gRoots(0, 2, -2)).

