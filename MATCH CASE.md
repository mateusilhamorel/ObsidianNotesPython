Sintaxe

O match case é uma estrutura para seleção de um caso (dentre vários), conforme um valor.
É o análogo do switch de outras linguagens.

```python
dia = 0
selecionado = "";

match day_number:  
	case 0:  
		selecionado = "Segunda - Inicio da semana"  
	case 1:  
		selecionado =  "Terça - Meio da semana"  
	case 2:  
		selecionado =  "Quarta - Ápice da semana"  
	case 3:  
		selecionado =  "Quinta - Quase lá!"  
	case 4:  
		selecionado =  "Sexta - Sextou!"  
	case 5 | 6: # Combine multiple cases with '|'  
		selecionado =  "Fim de semana!"  
	case _: # Wildcard case, acts as a default  
		selecionado =  "Invalid day number"
		
print(selecionado)
```