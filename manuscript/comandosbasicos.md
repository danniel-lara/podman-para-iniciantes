# Comandos básicos

Para utilização do Docker é necessário conhecer alguns comandos e entender de forma clara e direta para que servem, assim como alguns exemplos de uso.

Não abordaremos os comandos de criação de imagem e tratamento de problemas (troubleshooting) no Docker, pois têm capítulos específicos para o detalhamento.

# Ajuda 

Assim como a maioria dos comandos vem com a opção --help e no caso do Podman não é diferente 

```
podman --help
```

Exemplo

```
podman --help
Manage pods, containers and images

Usage:
  podman [options] [command]

Available Commands:
  attach      Attach to a running container
  auto-update Auto update containers according to their auto-update policy
  build       Build an image using instructions from Containerfiles
  commit      Create new image based on the changed container
  container   Manage containers
  cp          Copy files/folders between a container and the local filesystem
  create      Create but do not start a container
  diff        Display the changes to the object's file system
  events      Show podman events
  exec        Run a process in a running container
  export      Export container's filesystem contents as a tar archive
  generate    Generate structured data based on containers, pods or volumes
  healthcheck Manage health checks on containers
  help        Help about any command
```

 O mesmo também para **podman run --help**, **podman image**, etc...


```
podman run --help
Run a command in a new container

Description:
  Runs a command in a new container from the given image

Usage:
  podman run [options] IMAGE [COMMAND [ARG...]]

Examples:
  podman run imageID ls -alF /etc
  podman run --network=host imageID dnf -y install java
  podman run --volume /var/hostdir:/var/ctrdir -i -t fedora /bin/bash

Options:
      --add-host strings                         Add a custom host-to-IP mapping (host:ip) (default [])
      --annotation strings                       Add annotations to container (key=value)
      --arch ARCH                                use ARCH instead of the architecture of the machine for choosing images
  -a, --attach strings                           Attach to STDIN, STDOUT or STDERR
      --authfile string                          Path of the authentication file. Use REGISTRY_AUTH_FILE environment variable to override
```

O help sempre nos ajuda a todo momento use com sabedoria.

# Info

O comando **podman info** Exibe informações do sistema relacionadas ao Podman como 
informações pertinentes ao host, estatísticas de armazenamento atuais, registros de contêiner configurados e compilação do podman.
Com o **podman info** podemos verificar o Registries, é nele onde mostra onde o podman irá buscar por containers, ele também 
pode ser visto no arquivo **/etc/containers/registries.conf** 

```
podman info -f '{{range index .Registries "search"}}{{.}}\n{{end}}'
registry.fedoraproject.org
registry.access.redhat.com
docker.io
quay.io
```


