Sintaxe

Para definir um atributo de uma classe como privado usa-se o " _ " em frente ao nome da variável.
Isso torna impossível a alteração do valor (manipulação) da variável por fora do objeto ou diretamente.

Para manipular a variável é necessário criar métodos internos ao objeto que permitam a manipulação através do "@property" .

```python
class Casa:

    def __init__(self, preco):
        self._preco = preco #É um atributo privado

    @property
    def preco(self):
        return self._preco

    @preco.setter
    def preco(self, novo_preco):
        if novo_preco > 0 and isinstance(novo_preco, float):
            self._preco = novo_preco
        else:
            print("Insira um preço válido")

    @preco.deleter
    def preco(self):
        del self._preco

  

casa = Casa(50000.0) # Criar instância

  
print("Preco:",casa.preco)
print("Troca preco com casa.preco=4500.0")
casa.preco=4500.0
print("Preco:", casa.preco)
print("Deletar preco com del casa.preco")
del casa.preco
```
 
Quando usamos o @property na função que retorna o preço, estamos indicando que a função se tornará um atributo da classe e poderá ser invocada através do operador "."

Depois usamos @preco.setter para definir a função que atribui o valor ao atributo preço.
Ao atribuir @preco.setter à função, ela se torna o setter do atributo. Isso indica que agora, quando fizer objeto.preco = valor não estaremos mais atribuindo diretamente o valor à variável, mas sim invocando a função definida como setter.

  Você ainda pode usar o @preco.delete para definir um método para excluir a propriedade usando o comando "del".
  
O decorador `@property` é muito útil em situações em que precisamos controlar o acesso aos atributos de uma classe.

Aqui estão alguns exemplos de casos de uso comuns:

- Conversão de tipos: podemos usar `@property` para converter automaticamente tipos de dados. Por exemplo, podemos ter um atributo `data` que é armazenado como uma string e uma propriedade `data` que devolve o valor convertido em um objeto `datetime`.

- Verificação de validade: podemos adicionar validações em um `setter` para garantir que os atributos estão dentro dos limites aceitáveis. Por exemplo, podemos ter um atributo `idade` que precisa ser um número positivo e, caso contrário, levanta um erro.

- Uso de cache: podemos utilizar uma propriedade para fazer cache de um valor calculado, evitando recalcular a cada vez que a propriedade é acessada.

- Acesso a dados externos: podemos usar propriedades para acessar e atualizar dados em bancos de dados externos ou sistemas remotos. Dessa forma, podemos manter a interface do objeto consistente, independentemente de onde os dados são armazenados.