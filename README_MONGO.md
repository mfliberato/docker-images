# MongoDB e Mongo Express com Docker Compose

Este repositório contém um exemplo de configuração para iniciar um MongoDB e o Mongo Express usando Docker Compose.

## Estrutura do Projeto

O projeto é composto pelos seguintes serviços:

1. **MongoDB**: Um banco de dados NoSQL.
2. **Mongo Express**: Uma interface web para o MongoDB.

## Requisitos

- [Docker](https://docs.docker.com/get-docker/) (versão 19.03.0 ou superior)
- [Docker Compose](https://docs.docker.com/compose/install/) (versão 1.25.0 ou superior)

## Como Usar

1. Clone este repositório:

   ```sh
   git clone https://github.com/mfliberato/docker-images.git
   
   cd your-repository
   
   Execute: docker-compose -f docker-compose.mongodb.yml up -d

   Acesse a interface: http://localhost:8081
