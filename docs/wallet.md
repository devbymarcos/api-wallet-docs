# Wallet

[Sumário](/README.md)


## `GET: /wallet`

Busca o usuário cadastrado baseado no seu id.
Nesse caso só é necessario o envio do token junto da requisição no cabeçalho

EXEMPLO :

```
{
  "Authorizarion": Bearer <seutoken aqui>,
}
```

## Response :

Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "id": 1,
  "first_name": "Pessoa",
  "last_name": "Sobrenome",
  "email": "Pessoa@gmail.com",
  "photo": "default"
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