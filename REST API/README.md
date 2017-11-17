# Konecty REST API

## Detalhes

Os métodos da API tem restrições conforme configuração de acesso do usuário qual esta sendo enviado Token.

## Autenticação

Para realizar qualquer busca dentro do konecty, deve ser primeiro requisitado o token no método de autenticação e o mesmo ser enviado em todas as outras posteriores.

Para maior detalhes acesse o [link](Authentication/)

## Request


## Lista de métodos

| URL                                                               | Descrição                                       | Detalhes              |
|-------------------------------------------------------------------|-------------------------------------------------|:---------------------:|
| `https://[dominio.konecty]/rest/data/:document/find`              | Lista de dados referente ao ':document' passado |[Link](Find/)|
| `https://[dominio.konecty]/rest/data/:document/:dataId`           | Busca o '_id' referente ao ':document' passado  |[Link](Find/ById/)|

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