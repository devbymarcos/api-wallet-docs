# User

[Summário](/README.md)

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
  "first_name": "string",
  "last_name": "string",
  "email": "string",
  "photo": "string",
  "token": "string"
}
```

## `GET: /user`

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
  "first_name": "Marcos",
  "last_name": "Juvencio",
  "email": "marcoslopes.dev@gmail.com",
  "photo": "default"
}

```

<a id="login"></a>
