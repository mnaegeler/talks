# Exemplo 1

1 - Verificar se o docker está instalado e rodando

```
➜  orquestrando-containers-com-docker git:(master) ✗ docker version
Client:
 Version:      18.03.1-ce
 API version:  1.37
 Go version:   go1.9.5
 Git commit:   9ee9f40
 Built:        Thu Apr 26 07:13:02 2018
 OS/Arch:      darwin/amd64
 Experimental: false
 Orchestrator: swarm

Server:
 Engine:
  Version:      18.03.1-ce
  API version:  1.37 (minimum version 1.12)
  Go version:   go1.9.5
  Git commit:   9ee9f40
  Built:        Thu Apr 26 07:22:38 2018
  OS/Arch:      linux/amd64
  Experimental: true
```

2 - Executar o hello world

```
➜  website git:(al-code-update-to-rails5.1.6) docker run hello-world

Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
9bb5a5d4561a: Pull complete
Digest: sha256:f5233545e43561214ca4891fd1157e1c3c563316ed8e237750d59bde73361e77
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/engine/userguide/
```



3 - Executar um container

`docker run ubuntu echo "Ola Mundo"`


```
➜  orquestrando-containers-com-docker git:(master) ✗ docker run ubuntu

➜  orquestrando-containers-com-docker git:(master) ✗ docker ps -a
CONTAINER ID        IMAGE                       COMMAND                  CREATED                  STATUS                      PORTS                    NAMES
b4bc4138a5b5        ubuntu                      "/bin/bash"              Less than a second ago   Exited (0) 1 second ago                              boring_carson
```

Isso ocorre pois para que um container fique no ar, ele necessariamente precisa conter um processo rodando. Como o que está sendo chamado não executa nada, e abre no terminal, ele mata o container em seguida.

No seguinte link ->
https://github.com/docker-library/repo-info/blob/master/repos/ubuntu/local/16.04.md, podemos ver que na documentação deste container, o que executa é o `/bin/bash`, logo, o bash não é um serviço que segure um container.

Se eu executo um comando como por exemplo `docker run ubuntu sleep infinity`, ele vai deixar o container dormir eternamente, logo, ele aparecerá no docker PS com o serviço que está executando.

```
CONTAINER ID        IMAGE                      COMMAND                  CREATED                  STATUS              PORTS                    NAMES
55372585a606        ubuntu                     "sleep infinity"         Less than a second ago   Up 10 seconds                                inspiring_hypatia
```

E para matar este container:

```
CONTAINER ID        IMAGE                      COMMAND                  CREATED                  STATUS              PORTS                    NAMES
55372585a606        ubuntu                     "sleep infinity"         Less than a second ago   Up 10 seconds                                inspiring_hypatia
```


Pega o ID e executa o seguinte comando `docker rm -f 55372585a606`

```
➜  listing-api git:(master) docker ps
CONTAINER ID        IMAGE                      COMMAND                  CREATED             STATUS              PORTS                    NAMES
```

4 - Rodando ubuntu no terminal

Utilizando o comando com o `-it`, ele irá executar o que está especificado para que seja executado, e irá segurar o terminal com aquele processo.

```
➜  orquestrando-containers-com-docker git:(master) ✗ docker run -it ubuntu
root@2336be2469b1:/#
```

5 - Remover todas as imagens paradas

`docker container prune`