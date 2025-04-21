# 🐳 Comandos Docker Essenciais

## Imagens

- `docker pull <imagem>`  
  Baixa uma imagem do Docker Hub.

- `docker images`  
  Lista as imagens disponíveis localmente.

- `docker rmi <imagem>`  
  Remove uma imagem local.

- `docker build -t <nome>:<tag> .`  
  Cria uma imagem a partir de um Dockerfile.

---

## Containers

- `docker run <imagem>`  
  Executa um container com a imagem especificada.

- `docker run -d <imagem>`  
  Executa o container em segundo plano (detached).

- `docker run -it <imagem>`  
  Executa o container no modo interativo com terminal.

- `docker run --name <nome> <imagem>`  
  Executa o container com um nome personalizado.

- `docker ps`  
  Lista os containers em execução.

- `docker ps -a`  
  Lista todos os containers (inclusive os parados).

- `docker start <nome/id>`  
  Inicia um container parado.

- `docker stop <nome/id>`  
  Para um container em execução.

- `docker restart <nome/id>`  
  Reinicia um container.

- `docker rm <nome/id>`  
  Remove um container (precisa estar parado).

- `docker exec -it <nome/id> bash`  
  Acessa o terminal bash dentro do container.

---

## 📁 Volumes e Arquivos

- `docker run -v <host>:<container> <imagem>`  
  Monta um volume (ex: `-v $(pwd):/app`).

- `docker cp <origem> <destino>`  
  Copia arquivos de/para o container.  
  Ex: `docker cp arquivo.txt container:/app`

---

## 🧰 Outros comandos úteis

- `docker logs <nome/id>`  
  Exibe os logs do container.

- `docker inspect <nome/id>`  
  Exibe detalhes técnicos do container ou imagem.

- `docker network ls`  
  Lista redes Docker.

- `docker volume ls`  
  Lista volumes Docker.

- `docker system prune`  
  Remove recursos não utilizados (⚠️ use com cuidado!).

---

