# Roteiro

 - Apresentação sobre o que é o docker (10m)
 - Apresentação dos comandos básicos do docker (15m)
    - Versão (de acordo com data)
    - `docker ps` && `docker ps -a`
    - `docker run hello-world`
    - Sem setar o volume `docker run ubuntu`
    - Imagem do ubuntu no dockerhub (https://hub.docker.com/_/ubuntu/)
    - Sem setar o volume `docker run -v /var/www ubuntu`
    - Setando o volume `docker run ubuntu -v ${PWD}:/var/www`
    - `docker inspect ID_DO_CONTAINER`
    - Aplicação de teste `docker run -d -P dockersamples/static-site`
    - Aplicação em nodeJS `docker run -p 8080:3000 -v "$(pwd):/var/www" -w "/var/www" node npm start`
    - Imagem do node no dockerhub (https://hub.docker.com/_/node/)
- Apresentação do compose e dockerfiles (20m)
  - Mostrar Dockerfile
  - Mostrar Dockerfile-ex-1
  - Mostrar Dockerfile-ex-2
  - Mostrar docker-compose da aplicação ex-sp-node
  - Mostrar docker-compose do PHP
  - Motrar dockerfile do my_favorite_friend
