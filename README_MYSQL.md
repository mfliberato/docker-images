# MySQL Docker Compose Setup

Este repositório contém uma configuração de `docker-compose.yml` para criar um ambiente de testes com o banco de dados MySQL usando Docker. Ele é ideal para equipes de desenvolvimento que precisam de um ambiente de banco de dados rápido e fácil de configurar.

## Pré-requisitos

- [Docker](https://www.docker.com/get-started) e [Docker Compose](https://docs.docker.com/compose/install/) instalados em sua máquina.

## Configuração

O arquivo `docker-compose.mysql.yml` neste repositório define um serviço para um container MySQL. Aqui estão os detalhes:

- **Imagem**: `mysql:8.0`
- **Nome do Container**: `mysql-test`
- **Porta**: `3306` (padrão MySQL)
- **Volume**: `mysql_data` mapeado para `/var/lib/mysql` no container para persistência de dados
- **Rede**: `mysql_network` para isolamento de rede

### Variáveis de Ambiente

O container usa as seguintes variáveis de ambiente para configuração:

- `MYSQL_ROOT_PASSWORD`: Senha para o usuário root.
- `MYSQL_DATABASE`: Nome do banco de dados inicial a ser criado.
- `MYSQL_USER`: Nome do usuário padrão.
- `MYSQL_PASSWORD`: Senha para o usuário padrão.

Você pode modificar essas variáveis diretamente no arquivo `docker-compose.mysql.yml` conforme necessário.

## Instruções de Uso

### 1. Subir o Ambiente

Para iniciar o ambiente MySQL, execute o comando abaixo:

```bash
docker-compose -f docker-compose.mysql.yml up -d
