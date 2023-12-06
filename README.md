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

- ```go mod tidy```
  - Usado para garantir que o arquivo go.mod reflita precisamente as dependências do código presente

- ```go test ./...```
  - Usado para rodar os testes do Go.

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