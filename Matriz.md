Sintaxe

Matrizes são vetores de mais de uma dimensão.
Matrizes não são nativas do Python e é necessário instalar um pacote para usar as matrizes.
Caso não tenha visto pacotes ainda siga para [[Ambiente virtual]] e depois para  [[Imports]] e  [[Pacotes]]

O pacote em questão é o "numpy".

```python
#Necessario criar um ambiente e instalar o numpy com o pip.

import numpy as np

matriz = np.array([[2, 3, 1], [4, 5, 7]])

print(matriz)
print(matriz.shape)
print(matriz[0])
print(matriz[0,0])
print(matriz[0,1])
print(matriz[0,2])
print()
print()

print(matriz)
print(matriz.shape)
print(matriz[0])
print(matriz[0][0])
print(matriz[0][1])
print(matriz[0][2])
print()
print()

for i in range(matriz.shape[0]):
    for j in range(matriz.shape[1]):
        print(matriz[i][j])
```
