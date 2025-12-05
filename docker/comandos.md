# 🐳 Docker — Comandos Principais

> Documento de referência rápida com os comandos mais usados no dia a dia.

---

## 📌 Docker — Comandos Essenciais

### 🔍 Informações e Status
```bash
docker --version
docker info
docker ps           # containers em execução
docker ps -a        # todos os containers (inclusive parados)
docker images       # lista imagens locais
docker volume ls    # lista volumes
docker network ls   # lista redes
```

## 💿 Imagens
```bash
docker pull <imagem>          # baixa imagem
docker build -t nome:tag .    # cria imagem a partir de Dockerfile
docker rmi <imagem>           # remove imagem
docker images prune           # remove imagens não utilizadas
```


## 🧰 Containers
```bash
docker run <imagem>                   # executa container
docker run -d <imagem>                # executa em background
docker run -p 8080:80 <imagem>        # mapeia portas
docker run --name meuapp <imagem>     # define nome

docker stop <container>               # para container
docker start <container>              # inicia container parado
docker restart <container>            # reinicia
docker rm <container>                 # remove container
docker rm -f <container>              # força remoção
```

## 📦 Executando comandos dentro do container
```bash
docker exec -it <container> bash      # abre terminal interativo (Linux)
docker exec -it <container> sh        # terminal alternativo
docker logs <container>               # mostra logs
docker logs -f <container>            # segue logs em tempo real
```

## 🧼 Limpeza
```bash
docker system prune            # remove recursos não usados
docker system prune -a         # remove tudo (cuidado!)
docker container prune         # remove containers parados
docker volume prune            # remove volumes não usados
```

## 🔗 Documentação oficial
- https://docs.docker.com