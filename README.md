# API PARA ESTUDOS WALLETCONTROL

WC é um controlador financeiro para gerenciar despesas e receitas. O objetivo é que toda receita ou despesa esteja vinculada a uma carteira, ou seja, toda a visualização de dados e persistência estão diretamente ligadas à carteira selecionada.

Portanto, toda movimentação de `Receita` ou `Despesa` precisa incluir um `walletID`, que representa a carteira que receberá o registro

## Instruções Primarias

- Para realizar requisições você pode utilizar um cliente como **Insomnia** ou o **Postman**.
- O Sumário vai ajudar a navegar na documentação.
- Todos os envios devem serm no formato `json` ou seja `Content-type:application/json`.

<a id="inicio"></a>

## Sumário

Endpoints

- [User](docs/user.md)

### URL BASE

Por gentileza essa api é apenas para testes. Qualquer informação persistente será removido

```
http://localhost:4000/v1
```

# User

<a href="#inicio">SUMÁRIO</a>

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

## Login

<a href="#inicio">Voltar para o Início</a>

### Verifica os dados e devolve o `token`.

### Ponto de acesso / endpoint

`POST` **`/login`**

**Request body:**

Você deve enviar os dados no corpo da requisição

```
{
    "email": "email@alteraroemail.com",
    "passwd" : "senha-aqui"
}
```

### Schema

```
    {
        "email": string,
        "passwd" : string
    }
```

**Response:**

Você pode obter as seguintes respostas

- `200` description `ok`
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

- `204` usuário nao encontrado
