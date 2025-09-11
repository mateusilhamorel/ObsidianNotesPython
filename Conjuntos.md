Sintaxe

Os conjuntos são dicionários sem índice. [[Dicionários]]
Sendo assim, um conjunto é NÃO ORDENADO.
Os elementos não podem ser acessados por índice.
Cada elemento é único no conjunto, não há repetições.
O conjunto é mutável (ou seja, ele pode adicionar ou remover elementos após sua criação.)

Conjuntos são uteis para:

- **Remover duplicatas:** É uma forma eficiente de obter apenas elementos únicos de uma lista. 
- **Verificar a existência de um elemento:** A verificação de pertencimento ( `in` ) em conjuntos é mais rápida do que em listas, especialmente para conjuntos grandes. 
- **Realizar operações matemáticas:** Para aplicar conceitos como união, interseção e diferença.

```python
print("conjunto = {1, 2, 3, 4, 5, 5, 5, 5}")
conjunto = {1, 2, 3, 4, 5, 5, 5, 5}
print(type(conjunto))
print(conjunto)
```




