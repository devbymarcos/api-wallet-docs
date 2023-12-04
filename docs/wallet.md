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
  "wallets": [
    {
      "description": "cartão de crédito",
      "name": "Mercado card - Cartão"
    },
    {
      "description": "Despesas com cartão",
      "name": "card-card"
    },
    {
      "description": "cartao",
      "name": "card-banks"
    }
  ]
}

```

ou

```
{
  "data": null,
  "message": "não encontramos o resgistro "
}

```
## `GET: /wallet/{id}`

Retorna carteira para o id do parametro


Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "wallet": {
    "description": "cartão de crédito",
    "name": "bancoX - Cartão",
    "option_wallet": 0
  }
} 

```
ou

```
{
  "data": null,
  "message": "não encontramos o resgistro "
}

```

## `POST: /wallet`

Cria uma nova carteira

EXEMPLO :

```
{
  "user_di": "1",
  "name": "carteira nome",
  "description": "despesas gerais",
  "option_wallet": "1 - usar como preferencia  0 - para não preferencia"
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
  wallet:{
  "user_id": "int",
  "name": "string",
  "description": "string",
  "option_wallet": "int"
  }
}  

```


## `PUT: /wallet/{id}`

Atualiza a carteira com base no id 

EXEMPLO :

``` 
{
  "id": "int",
  "name": "string",
  "description": "string",
  "option_wallet": "int"
}

```

## Response :

Se tudo correr bem você tera um `json` com dados atualizados

Code `200` description `ok`

Tipo: `application/json`

```
{ 
  wallet:{
  "name": "string",
  "description": "string",
  "option_wallet": "int"
  }
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
  "message": exclusao realizda,
  "execute": true
}  

```