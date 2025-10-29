Sintaxe

Serve para fazer busca sofisticada por padrões.

Métodos usados: 

search: Encontra posições de padrões dentro de strings.

match: Encontra se o começo de uma string é igual a um determinado padrão.

findall: encontra todas as substrings que correspondem a um padrão.

Metacaracteres:

"." Qualquer caractere (exceto linha nova).
"\w" Qualquer caractere ALFANUMERICO.
"\W" Qualquer caractere NÃO-ALFANUMERICO.
"\d"  Qualquer caractere que SEJA DÍGITO.
"\D" Qualquer caractere que NÃO SEJA DÍGITO.
"\s" Espaço em branco.
"^" Deve começar com ...
"$" Deve terminar com ...
" \ " Usado entes dos Metacaracteres para especificar seu significado literal (usar o símbolo do metacaractere na busca) 


Quantificadores:
(Permitem determinar como e quantas vezes os metacaracteres aparecem.)

[ ]  opcional entre os que estão dentro dos colchetes
( ) captura grupos de caracteres
" * " de zero a mais vezes
" ? " zero ou uma vez
" + " uma ou mais vezes
{m , n} de m a n vezes
| logico OU


```python
import re

frase1_search = 'Olá, meu numero de telefone é (42) 9867-9867'
print(re.search(r'\(\d{2}\) \d{4}-\d{4}', frase1_search).group())

frase2_search = 'A placa do carro que eu anotei durante o acidente foi FRT-1998'
print(re.search(r'[A-Z]{3}-\d{4}', frase2_search).group())
email_search = 'Entre em contato com teste@teste.com, ou com fcawf@gthell.com.us'
print(re.search(r'[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}', email_search).group())
print("re.search só puxa a primeira ocorrencia da busca!")

  

print()
frase1_match = 'A placa do carro que eu anotei durante a batida foi FRT-1998'
print(frase1_match)
print(re.match(r'[A-Z]{3}-\d{4}', frase1_match))  
print("re.match só funciona se o padrão estiver no começo da string!")

frase2_match = 'FRT-1998 é a placa do carro'
print(frase2_match)
print(re.match(r'[A-Z]{3}-\d{4}', frase2_match))

  

print()
frase_findall = 'Meus emails são fcawf@donotknow.com.us e para os mais chegados queroCafe@hotmail.com'
print(frase_findall)
print(re.findall(r'[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}', frase_findall))
```
```
```








