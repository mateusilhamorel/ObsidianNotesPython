Sintaxe

A estrutura WHILE é semelhante ao FOR.

A estrutura executa o bloco de comandos até que encontra um critério de parada (que deve ser definido dentro do bloco de comandos a ser executado).
A estrutura WHILE deve ser usada com cuidado. Se o critério de parada não for cuidadosamente definido, a estrutura pode entrar em modo loop infinito e comer a memória do sistema.


```python
contador = 0  # Inicializa uma variável de contagem
while contador < 5:
    print(contador)
    contador += 1 # Incrementa o contador a cada iteração

print("Laço concluído!")
```

