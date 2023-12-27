# User

[Sumário](/README.md)

## `GET: /user`

Busca o usuário cadastrado baseado no seu id.
Nesse caso só é necessario o envio do token junto da requisição no cabeçalho

EXEMPLO :

```
{
  "Authorizarion": Bearer <seutokenaqui>,
}
```

## Response :

Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 1,
    "first_name": "Name",
    "last_name": "LastName",
    "email": "umemail@seudominio.com",
    "photo": "default"
  },
  "message": "",
  "request": "user"
}

```

## `POST: /user`

Cria um novo usuário

EXEMPLO :

```
{
  "first_name": "seu nome",
  "last_name": "seu sobrenome",
  "email": "email@email.com",
}
```

### Schema

```
    {
        "first_name": "string",
        "last_name": "string",
        "email": "string",
    }
```

## Response :

Você pode obter as seguintes respostas

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 1,
    "first_name": "Name",
    "last_name": "LastName",
    "email": "umemail@seudominio.com",
    "photo": "default"
  },
  "message": "",
  "request": "user"
}
```

## `PUT: /user`

Atualiza informação do usuário registrado.

EXEMPLO :

```
{
  "first_name": "NovoNome",
  "last_name": "NovoSobreNome",
  "email": "NovoEmail@gmail.com",
  "photo": "default"
}
```

## Response :

Se tudo correr bem você tera um `json` com dados atualizados

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": {
    "id": 1,
    "first_name": "Name",
    "last_name": "LastName",
    "email": "umemail@seudominio.com",
    "photo": "default"
  },
  "message": "",
  "request": "user"
}

```

## `PUT: /userpass`

Atualiza senha do usuario logado.

EXEMPLO :

```
{
  "password": "novasenha",

}
```

## Response :

Se tudo correr bem você tera um `json` com dados atualizados

Code `200` description `ok`

Tipo: `application/json`

```
{
  "data": true
}

```
