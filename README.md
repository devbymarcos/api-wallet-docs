# API PARA ESTUDOS WALLETCONTROL

WC é um controlador financeiro para gerenciar despesas e receitas. O objetivo é que toda receita ou despesa esteja vinculada a uma carteira, ou seja, toda a visualização de dados e persistência estão diretamente ligadas à carteira selecionada.

Portanto, toda movimentação de `Receita` ou `Despesa` precisa incluir um `walletID`, que representa a carteira que receberá o registro

## Instruções Primarias

- Para realizar requisições você pode utilizar um cliente como **Insomnia** ou o **Postman**.
- O Sumário vai ajudar a navegar na documentação.
- Todos os envios devem serm no formato `json` ou seja `Content-type:application/json`.

## Sumário

Endpoints

- [User](docs/user.md)
- [Wallet](docs/wallet.md)

### URL BASE

Por gentileza essa api é apenas para testes. Qualquer informação persistente será removido

```
http://localhost:4000/v1
```
