# Exemplo 3

docker run dockersamples/static-site
docker ps
docker run -d dockersamples/static-site
docker ps
docker run -d -P dockersamples/static-site
docker port ID_CONTAINER



#
para todos os containers docker stop -t 0 $(docker ps -q)



# Rodando uma aplicação de exemplo em node

https://github.com/nodejs/docker-node/blob/master/README.md#how-to-use-this-image

docker run -p 8080:3000 -v "$(pwd):/var/www" -w "/var/www" node npm start
