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

# Adiciona o Python ao gerenciador de pacotes
$ sudo apt-add-repository ppa:deadsnakes/ppa -y

# Atualiza os pacotes
$ sudo apt-get update

# Instala o Python 3
$ sudo apt-get install -y python3-dev python3-distutils python3-pip

# Instala o virtualenv
$ pip3 install virtualenv

# Cria o ambiente virtual
$ python3 -m venv ~/venv

# Ativa o ambiente virtual
$ . ~/venv/bin/activate
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
