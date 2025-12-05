# 🐳 Docker Compose — Comandos Principais

## ▶️ Iniciar e Parar

```bash
docker-compose up               # sobe serviços
docker-compose up -d            # sobe em background
docker-compose down             # para e remove containers
docker-compose restart          # reinicia serviços
```

## 🔧💿 Construção e Imagens
```bash
docker-compose build            # build manual
docker-compose up --build       # sobe e recria imagens
docker-compose pull             # baixa imagens definidas
```

## 📄 Informações
```bash
docker-compose ps               # status dos serviços
docker-compose logs             # logs de todos serviços
docker-compose logs -f          # segue logs
docker-compose config           # valida e mostra merge do yaml
```

## 🧹 Limpeza
```bash
docker-compose down -v          # remove volumes
docker-compose rm               # remove containers gerenciados
```

## 📁 Estrutura exemplo de docker-compose.yml

```bash
version: "3.9"

services:
  api:
    image: node:18
    container_name: api-node
    working_dir: /app
    volumes:
      - .:/app
    command: npm start
    ports:
      - "3000:3000"
    depends_on:
      - db

  db:
    image: postgres:15
    container_name: db-postgres
    environment:
      POSTGRES_USER: user
      POSTGRES_PASSWORD: pass
      POSTGRES_DB: minha_base
    ports:
      - "5432:5432"
```

## 🧠 Dicas úteis
✔ Sempre nomeie containers com `--name` <br>
✔ Use `.env` no mesmo diretório do `docker-compose.yml` <br>
✔ Evite usar `latest` em ambientes produtivos <br>
✔ Use volumes para persistir dados de banco

## 🔗 Documentação oficial
- https://docs.docker.com/compose








<!-- ```yaml
services:
  sql:
    image: mcr.microsoft.com/mssql/server
``` -->
