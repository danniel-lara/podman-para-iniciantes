# Instalação

O Podman pode ser instalado em Windows , Mac e Linux

## Instalação no GNU/Linux

Instalações por Distribuições 

# Arch Linux e Manjaro Linux

```
sudo pacman -S podman
```

# Alpine Linux

```
sudo apk add podman
```

# Centos 
O Podman está disponével nos repositórios Extras padrão Centos 7 e no repositório AppStream para Centos8 e Stream.

```
sudo yum -y install podman
```

# Debian

O pacote está disponível nos repositórios Debian 11 (Bullseye) e Posterioes.

```
sudo apt-get install -y podman
```

# Fedora 

Conforma a instalação do Fedora ele já vem instalado por padrão ,
No Fedora Silverblue e Fedora CoreOS já vem por padrão o podman no instalação

```
sudo dnf install podman -y
```

# Gentoo

```
sudo emerge app-containers/podman
```

# OpenSUSE

```
sudo zypper install podman
```

# RHEL7

Inscreva-se, ative o canal Extras e instale o Podman.

```
sudo subscription-manager repos --enable=rhel-7-server-extras-rpms
sudo yum -y install podman
```

# RHEL8

O Podman está incluído no container-toolsmódulo, juntamente com o Buildah e o Skopeo.
```
sudo yum module enable -y container-tools:rhel8
sudo yum module install -y container-tools:rhel8
```

O container-tools:rhel8 é o fluxo de aplicativo rápido, contendo as versões contínuas mais recentes das ferramentas. Use o container-tools:2.0stream para versões estáveisdo Podman 1.6. O comando "yum module list container-tools" mostra os fluxos disponíveis.

# Ubuntu

O pacote podman está disponível nos repositórios oficiais do Ubuntu 20.10 e mais recentes.

```
# Ubuntu 20.10 and newer
sudo apt-get -y update
sudo apt-get -y install podman
```






