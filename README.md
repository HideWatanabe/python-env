# Instalação do ambiente Python do Wata
## O que iremos instalar?
- [x] pyenv
- [x] venv

## Observações iniciais:
- SO: Ubuntu 19.10

### pyenv
pyenv é uma ferramenta de gerenciamento de versão do Python, também conhecida como Pythonbrew. Essa ferramenta possibilita a instalação de múltiplas versões de Python em uma máquina, possibilitando, de maneira simples e fácil, trocar entre as versões instaladas.

#### Instalação do pyenv:
##### Pré-requisitos:
Os pré-requisitos estão no apt abaixo:
```shell
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```
##### Instalação da maneira easy:
```shell
curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash
```
##### Instalação da maneira menos easy:
```shell
cd
git clone git://github.com/yyuu/pyenv.git .pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
source ~/.bashrc
```
#### Comandos! =)
```shell
# Listagem de versões instaladas na máquina
pyenv versions
# Listagem de versões disponibilizadas para serem baixadas pelo pyenv
pyenv install -l
# Instalar determinada versão do Python pelo pyenv (Ex: 3.7.5)
pyenv install 3.7.5
# Utilizar alguma versão instalada do Python pelo pyenv como versão global da máquina (Ex: 3.7.5)
pyenv global 3.7.5
```

#### Links:
- [Tutorial](https://amaral.northwestern.edu/resources/guides/pyenv-tutorial)
- [Troubleshooting](https://github.com/pyenv/pyenv/wiki/Common-build-problems)


### virtualenv
virtualenv é um conceito/ferramenta para gestão de ambientes por contexto. Com ele é possível isolar o contexto de determinada aplicação com relação as dependências Python do projeto.

#### Pré-requisitos
Somente o Python3

#### Instalação
```shell
sudo apt install python3-venv
```

#### Comandos! =)
```shell
# Criação de contexto para determinada aplicação/pacote - Desde a versão 3.6 a execução do comando 'venv' sem estar explícito a utilização da versão 3 do Python está depreciada.
python3 -m venv .venv
# Ativação do ambiente isolado que criado anteriormente
source .venv/bin/activate
# Desativar o ambiente isolado
deactivate
```

#### Links
-[Utilização](https://docs.python.org/3/library/venv.html#module-venv)

#####