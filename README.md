# 🐳 Comandos Docker Essenciais

## Execuntando um Contêiner

```bash
docker pull ubuntu
docker run ubuntu
docker run ubuntu sleep 10
docker run ubuntu sleep 1500
docker stop [id]
docker run --help
docker run -it ubuntu

```

---

## Execuntando aplicação no Contêiner

```bash
docker run -dti  ubuntu 
docker exec -it [id ou nome]  /bin/bash
```

---

## Excluindo e nomeando contêiner

```bash
docker stop [id]
docker rm [id]
docker rmi [imagem]

docker run -dti --name Ubuntu-A ubuntu
```

## Copiando arquivos para um contêiner

```bash
docker exec -ti Ubuntu-A /bin/bash
docker exec Ubuntu-A mkdir /destino/
docker exec Ubuntu-A mkdir ls -l /
nano Arquivo.txt
docker cp arquivo.txt Ubuntu-A:/aula/
```

## Criando um Contêiner do MySQL

```bash
docker pull mysql
 
docker run -e MYSQL_ROOT_PASSWORD=Senha123 --name mysql-A -d -p 3306:3306 mysql

docker exec -it mysql-A bash

mysql -u root -p --protocol=tcp


CREATE DATABASE aula;
show databases;

docker inspect mysql-A

mysql -u root -p --protocol=tcp
```

