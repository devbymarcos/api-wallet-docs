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
  "first_name": "Pessoa",
  "last_name": "Sobrenome",
  "email": "Pessoa@gmail.com",
  "photo": "default"
}

```

## `PUT: /user`

Atualiza informação do usuário registrado.
a `password` só vai ser atualizado se voce enviar.

EXEMPLO :

```
{

  "first_name": "NovoNome",
  "last_name": "NovoSobreNome",
  "email": "NovoEmail@gmail.com",
  "photo": "default"
  "password": "NovaSenha
}
```

## Response :

Se tudo correr bem você tera um `json` com dados atualizados

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
