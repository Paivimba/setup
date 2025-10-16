# Guia de Instalação

## # Pré Requisitos

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala os pré-requisitos
$ sudo apt-get install ca-certificates curl gnupg lsb-release
```

## # Java

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instalação do pacote JDK
$ sudo apt-get install default-jdk

# Instalação do pacote JRE
$ sudo apt-get install default-jre
```

## # Python

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Dependências
$ sudo apt install -y build-essential curl git libssl-dev zlib1g-dev \
   libbz2-dev libreadline-dev libsqlite3-dev wget llvm libncurses5-dev \
   libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev

# Pyenv
$ curl https://pyenv.run | bash

# Configurar .zsh
# # Pyenv Setup
# export PYENV_ROOT="$HOME/.pyenv"
# export PATH="$PYENV_ROOT/bin:$PATH"
# if command -v pyenv 1>/dev/null 2>&1; then
#   eval "$(pyenv init --path)"
# fi
# if command -v pyenv 1>/dev/null 2>&1; then
#   eval "$(pyenv init -)"
# fi
# if command -v pyenv 1>/dev/null 2>&1; then
#   eval "$(pyenv virtualenv-init -)"
# fi

# Listar versões
$ pyenv install -l

# Instalar versão
$ pyenv install 3.13

# Criar ambiente virtual
$ pyenv virtualenv 3.13.9 global

# Definir versão global
$ pyenv global global

# Verificar versão
$ python -V
```

## # VSCode

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala o VSCode via Snap
$ sudo snap install --classic code
```

## # DBeaver

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala o DBeaver via Snap
$ sudo snap install dbeaver-ce
```

## [🔗](https://www.freecodecamp.org/news/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca/) Git

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala o git
$ sudo apt-get install git-all
```

## [🔗](https://docs.docker.com/engine/install/ubuntu/) Docker Engine

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Adiciona o docker ao gerenciador de pacotes
$ sudo install -m 0755 -d /etc/apt/keyrings
$ sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
$ sudo chmod a+r /etc/apt/keyrings/docker.asc
$ echo \
   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
   $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
   sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Atualiza os pacotes
$ sudo apt-get update

# Instala o Docker Engine
$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Cria um grupo de usuários Docker
$ sudo groupadd docker

# Adiciona o usuário ao grupo
$ sudo usermod -aG docker $USER

# Reinicia o computador
$ reboot

# Testando a instalação
$ docker run hello-world
```
