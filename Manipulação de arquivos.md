Sintaxe

Manipulação de arquivos para ler:

Para o texto abaixo considere que existe um arquivo texto.txt no caminho indicado.
O arquivo deve possuir pelo menos 4 linhas

```python
def lerArquivoCompleto(caminho):
    with open(caminho, 'r', encoding='utf-8') as tex:
        conteudo_total = tex.read()
        print(conteudo_total)


def lerArquivoLinha(caminho):
    with open(caminho, 'r', encoding='utf-8') as linha:
        lin = linha.readline()
        print(lin)


def lerLinhaEspecifica1(caminho, linha_desejada):
    ln = ''
    with open(caminho, 'r', encoding='utf-8') as tex:
        for numero, linha in enumerate(tex, start=0):
            if numero == linha_desejada:
                ln = (linha.strip())
                break
    return ln  


def lerLinhaEspecifica2(caminho, linha_desejada):
    with open(caminho, "r", encoding="utf-8") as f:
        linhas = f.readlines()
    return linhas[linha_desejada].strip()


def main():

    print("")
    caminho = r'D:\PY\PYTHON_BASE\ArquivosTexto\texto.txt'
    lerArquivoCompleto(caminho)
    print("")
    lerArquivoLinha(caminho)
    print("")
    print("Pega linha 2:")
    linha = lerLinhaEspecifica1(caminho, 1)    
    print(linha)
    print("")
    print("Pega linha 1:")
    linha = lerLinhaEspecifica2(caminho, 0)    
    print(linha)


main()
```

Manipulação de arquivos para escrever:

```python
def criaArquivoComTexto(nomeArquivo, texto):
    with open(nomeArquivo, 'w', encoding='utf-8') as text:
        text.write(texto)

def main():
    caminho = r'D:\PY\PYTHON_BASE\ArquivosTexto\texto2.txt'
    criaArquivoComTexto(caminho, 'Coloca o capacete que la vem pedrada!')    

main()
```