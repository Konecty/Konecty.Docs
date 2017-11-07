# Konecty REST API

## Detalhes

 Os métodos da API tem restrições conforme configuração de acesso do usuário qual esta sendo enviado Token.

## Autenticação

Para realizar qualquer busca dentro do konecty, deve ser primeiro requisitado o token no método de autenticação e o mesmo ser enviado em todas as outras posteriores.

Exemplo de requisição de Token de autenticação.

Realizando um POST para Url ```https://[domain]/rest/auth/login``` com o Header ```"Content-Type: application/json"``` e os parametros

``` 
{
    "user": "_LOGIN_",
    "password_SHA256": "_PASSWORD_SHA_256_",
    "ns": "[NAMESPACE]"
}
```

## Request

Para todos os requests, com exceção da autenticação, deve ser passar o Token de autenticação deve ser passado via Cookie.

## Lista de métodos

| URL                                                               | Descrição                                       | Detalhes              |
|-------------------------------------------------------------------|-------------------------------------------------|:---------------------:|
| `https://[dominio.konecty]/rest/data/:document/find`              | Lista de dados referente ao ':document' passado |[Link](/rest-api/find/)|
| `https://[dominio.konecty]/rest/data/:document/:dataId`           | Busca o '_id' referente ao ':document' passado  |[Link](/rest-api/find/byid/)|

## Lista de `:documents`

Lista de Documents do konecty

 - `Activity`
 - `AddressPlace`
 - `BankAccount`
 - `BankAccountTransaction`
 - `BlogPost`
 - `Campaign`
 - `CampaignTarget`
 - `CampaignUser`
 - `Channel`
 - `Contact`
 - `Contract`
 - `Dashboard`
 - `DataSource`
 - `Default`
 - `Development`
 - `Device`
 - `Document`
 - `Group`
 - `Message`
 - `Offer`
 - `Opportunity`
 - `Order`
 - `OrderItem`
 - `Preference`
 - `Product`
 - `ProductsPerOpportunities`
 - `Promotion`
 - `Queue`
 - `QueueUser`
 - `Role`
 - `SupportCase`
 - `Tag`
 - `Template`
 - `User`
 - `WebElement`
 - `Wiki`


 Uma lista em Json das collections utilizadas esta em [core.MetaObject.json](https://github.com/Konecty/Konecty/blob/master/packages/konmeta/metadata/core.MetaObject.json)