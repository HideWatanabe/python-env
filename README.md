# Instalação do ambiente Python do Wata
## O que iremos instalar?
- pyenv
- 

## Observações iniciais:
- SO: Ubuntu 19.10

### pyenv
pyenv é uma ferramenta de gerenciamento de versão do Python, também conhecida como Pythonbrew. Essa ferramenta possibilita a instalação de múltiplas versões de Python em uma máquina, possibilitando, de maneira simples e fácil, trocar entre as versões instaladas.

#### Instalação do pyenv:
##### Pré-requisitos:
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
##### Comandos! =)
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

##### Links:
- [Tutorial](https://amaral.northwestern.edu/resources/guides/pyenv-tutorial)
- [Troubleshooting](https://github.com/pyenv/pyenv/wiki/Common-build-problems)