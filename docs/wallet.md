# Wallet

[Sumário](/README.md)

## `GET: /wallets`

Retorna todas as carteiras para o usuário logado

## Response :

Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": [
    {
      "id": 2,
      "user_id": 1,
      "name": "minha carteira update",
      "description": "despesas gerais update",
      "option_wallet": 0,
      "created_at": "2023-10-31T16:58:23.000Z",
      "updated_at": "2023-12-27T08:53:52.000Z"
    },
    {
      "id": 4,
      "user_id": 1,
      "name": "Inter-card",
      "description": "Despesas com cartão",
      "option_wallet": 0,
      "created_at": "2023-11-06T10:45:55.000Z",
      "updated_at": null
    },

  ],
  "message": "",
  "request": "wallet"
}

```

## `GET: /wallet/{id}`

Retorna carteira para o id

## Response :

Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 2,
    "user_id": 1,
    "name": "minha carteira update",
    "description": "despesas gerais update",
    "option_wallet": 0,
    "created_at": "2023-10-31T16:58:23.000Z",
    "updated_at": "2023-12-27T08:53:52.000Z"
  },
  "message": "",
  "request": "wallet"
}

```

## `POST: /wallet`

Cria uma nova carteira

EXEMPLO :

```
{
  "name":"minha fatura inter",
  "description":"controle de despesas do cartao",
  "option_wallet":"0"
}
```

### Schema

```
{
  "user_id": "int",
  "name": "string",
  "description": "string",
  "option_wallet": "int"
}
```

## Response :

Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 2,
    "user_id": 1,
    "name": "minha carteira update",
    "description": "despesas gerais update",
    "option_wallet": 0,
    "created_at": "2023-10-31T16:58:23.000Z",
    "updated_at": "2023-12-27T08:53:52.000Z"
  },
  "message": "",
  "request": "wallet"
}

```

## `PUT: /wallet`

Atualiza a carteira com base no id

EXEMPLO :

```
{
  "id" : "2",
  "name":"minha carteira update",
  "description":"despesas gerais update",
  "option_wallet":"0"
}

```

## Response :

Se tudo correr bem você tera um `json` com dados atualizados

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 2,
    "user_id": 1,
    "name": "minha carteira update",
    "description": "despesas gerais update",
    "option_wallet": 0,
    "created_at": "2023-10-31T16:58:23.000Z",
    "updated_at": "2023-12-27T08:53:52.000Z"
  },
  "message": "",
  "request": "wallet"
}

```

## `DELETE: /wallet/{id}`

Remove a carteira

### ATENÇÃO : TODOS OS REGISTRO VINCULADOS A CARTEIRA TAMBÉM SERÃO REMOVIDOS

EXEMPLO :

```
#ENVIE O ID DA CARTEIRA A SER EXCLUIDA COMO PARAMATRO DA ROTA

"wallet/2"

```

## Response :

Se tudo correr bem você tera um `json` com dados atualizados

Code `200 ` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 43,
    "user_id": 1,
    "name": "minha fatura",
    "description": "constrole de despesas",
    "option_wallet": 0,
    "created_at": "2023-12-27T12:14:53.000Z",
    "updated_at": null
  },
  "message": "item removido",
  "request": "wallet"
}

```
