run with `docker-compose up --build`

stops with `docker-compose down`

Execute mysql dump `docker-compose exec mariadb mysqldump db > dump.sql`


```
➜  ex-compose-php git:(master) ✗ docker-compose up --build
Creating network "ex-compose-php_default" with the default driver
Pulling mariadb (mariadb:latest)...
latest: Pulling from library/mariadb
3d77ce4481b1: Pull complete
4f6a779d83f5: Pull complete
8c1d272f25d5: Pull complete
672dd5e0b768: Waiting
84a7291b5996: Waiting
92edc8e8d33d: Download complete
f86a82067817: Download complete
8eff7352c12e: Download complete
705e5fd937c3: Downloading [======>                                            ]  10.71MB/76.55MB
8e85dd313344: Waiting
7e01ce16c2fa: Waiting
```
