# Imersão FullCycle

### Projeto Prático

Desenvolveremo uma plataforma de investimentos com Home Broker:

→ Sitema da Bolssa ( Simular uma B3 - Dar Match de ofertas de compra e vendas de ações )

→ Home Broker onde as ofertas serão submetidas, além dos indicadores em tempo real.

### Tecnologias

- Docker
- Linguagem Go
- Nest.js
- Next.js
- Apache Kafka
- SSE ( Server Sent Events )

### Comandos úteis


- ```cd go```
  - Entra na pasta do Projet em Golang

- ```go mod tidy```
  - Usado para garantir que o arquivo go.mod reflita precisamente as dependências do código presente

- ```go test ./...```
  - Usado para rodar os testes do Go.

- ```go run cmd/trade/main.go```
  - Usado para rodar o Projeto.
_____

### Kafka control-center

Ainda no repositório do go, inicie o docker compose

- ```docker-compose up -d```
  - Usado para iniciar o Docker Compose
  - Iniciará na rota _http://localhost:9021_
_____

Vá em Topics e crie dois tópicos, 

- Topic name: **input**
- Topic name: **output**

Entre no Topic input, clique em _Messages_ e realize a Venda e a Compra das ações.

Exemplo de msg pra venda:

    {
      "order_id": "1",
      "investor_id": "Mari",
      "asset_id": "asset1",
      "current_shares": 10,
      "shares": 5,
      "price": 5.0,
      "order_type": "SELL"
    }

Exemplo de msg pra compra:

    {
      "investor_id": "Celia",
      "asset_id": "asset1",
      "current_shares": 0,
      "shares": 5,
      "price": 5.0,
      "order_type": "BUY"
    }

_____