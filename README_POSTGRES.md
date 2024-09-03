# Docker Compose para PostgreSQL

Este repositório contém um arquivo `docker-compose.postgres.yml` que configura um contêiner Docker para um banco de dados PostgreSQL. O Docker Compose permite a execução rápida de um ambiente PostgreSQL em contêineres para desenvolvimento, testes ou ambientes de produção simples.

## Pré-requisitos

- [Docker](https://www.docker.com/get-started) instalado.
- [Docker Compose](https://docs.docker.com/compose/install/) instalado.

## Configuração

O arquivo `docker-compose.postgres.yml` está configurado para usar a imagem oficial do PostgreSQL. Ele cria um contêiner para o banco de dados PostgreSQL com um volume persistente para armazenar dados.

### Variáveis de Ambiente

O arquivo `docker-compose.postgres.yml` inclui algumas variáveis de ambiente configuráveis para o PostgreSQL:

- `POSTGRES_USER`: O nome de usuário do banco de dados.
- `POSTGRES_PASSWORD`: A senha do usuário do banco de dados.
- `POSTGRES_DB`: O nome do banco de dados que será criado na inicialização.

### Exemplo de configuração

Por padrão, o `docker-compose.postgres.yml` está configurado com os seguintes valores:

```yaml
environment:
  POSTGRES_USER: your_user
  POSTGRES_PASSWORD: your_password
  POSTGRES_DB: your_database

## Instruções de Uso

### 1. Subir o Ambiente

Para iniciar o ambiente Postgres, execute o comando abaixo:

```bash
docker-compose -f docker-compose.postgres.yml up -d