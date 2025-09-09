O pip é o instalador/gerenciador de pacotes do Python.

Para conferir se o pip está instalado, entre em um terminal e digite:
python -m pip --version

Se o sistema responder com uma versão, então o pip está instalado.


Instalando pacotes:


DO REPOSITORIO GERAL
O pip vai instalar o pacote na pasta onde o comando estiver sendo rodado.

py -m pip install  <nome do pacote>
(pode ser python -m pip install  <nome do pacote>)


DE UM REPOSITORIO GIT HUB

py -m pip install git+https://github.com/pypa/sampleproject.git@main


DE UM ARQUIVO DE LISTA:

py -m pip install -r requirements.txt

Neste arquivo devem constar os pacotes e suas versões:
Exemplo:

Flask==2.3.3  
Jinja2>=3.1.2,<4.0  
SQLAlchemy==2.0.23  
python-dotenv==1.0.0


DESINSTALAR UM PACOTE:

py -m pip uninstall <nome do pacote>






