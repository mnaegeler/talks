# Exemplo 2

1 - Fazendo o upload desta máquina para o DockerHub

Vamos utilizar como exemploa máquina `Dockerfile-ex-1`

```

```
Remover imagem

`docker images` + `docker rmi nome_da_imagem`

```
➜  orquestrando-containers-com-docker git:(master) ✗ docker images
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
test                        latest              ba732038bc72        23 minutes ago      415MB

➜  orquestrando-containers-com-docker git:(master) ✗ docker rmi test
Untagged: test:latest
Deleted: sha256:ba732038bc724f667398a49ffc40635071fd623404ea9514ecd3b250ee7b0794
Deleted: sha256:0ccbde87c28c455f0359bff14d788e5956fca560aa27c46b79f5996855d7bacf
Deleted: sha256:b56cd9696e853f1069edfb185aef8a3d059625ffce2465ff23aa3b9d180b7a9b
```
