Sintaxe

O python foi pensado para ser "modular", ou seja, para que fosse possível separar a programação em pacotes.

Assim, podemos reutilizar o pacote em diversas partes do sistema evitando ter que reescrever diversas vezes o mesmo código, sendo mais fácil encontrar as rotinas e fazer a manutenção.

Podemos importar pacotes instalados e podemos gerar nosso próprios pacotes.
Para criar nossos próprios pacotes siga para [[Pacotes]].

Quando instalamos um pacote "externo" (que não fomos nós mesmos que criamos), primeiro devemos instalar esse pacote através do "[[Pip]]" por exemplo. (Vide [[Ambiente Virtual]] antes de instalar qualquer pacote.)

Após instalado o pacote, podemos usar seus recursos:

```python
import numpy as np
matriz = np.array([[2, 3, 1],  [4, 5, 7]])
```

No código acima, antes de importar o pacote numpy devemos instalá-lo com o pip.

No fonte importamos o numpy e nomeamos o pacote como "np".
Depois usamos um recurso com "np.array()".





