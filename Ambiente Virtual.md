Infraestrutura
Ambiente

O Ambiente virtual é importante porque evita "contaminar" a instalação do Python original com pacotes que são exclusivos de outros projetos.

Assim, quando criamos um ambiente virtual, podemos instalar diversos pacotes "Extra" sem alterar a instalação do python original.

Para instalar, use o pip, que é o instalador e gerenciador dos pacotes python. 


instale o pip (gerenciador de pacotes)

pip install venv

(se pedir para atualizar... atualize)
python.exe -m pip install --upgrade pip

(talvez o sistema Windows cause algum bloqueio para a instalação, caso aconteça, execute)
python.exe -m pip install --upgrade pip --user

(para criar o ambiente virtual :)
python -m venv <nome do ambiente>

(o Windows pode barrar novamente a execução por causa de politicas de execução de script restritas)
acesse https://go.microsoft.com/fwlink/?LinkID=135170 para avaliar se precisa trocar a politicas

Inicie o PowerShell do Windows como administrador

Aplique: Get-ExecutionPolicy
para saber qual a politica vigente

Aplique: Set-ExecutionPolicy -ExecutionPolicy <nome da nova politica>
Set-ExecutionPolicy -ExecutionPolicy Unrestricted
Set-ExecutionPolicy -ExecutionPolicy Restricted
para trocar para a nova politica 

Execute: <nome do ambiente virtual>\Scripts\activate 
ou apenas activate se estiver na pasta do ambiente.
para ativar o ambiente virtual

Execute: deactivate
para desativar o ambiente virtual e voltar para o ambiente padrão.