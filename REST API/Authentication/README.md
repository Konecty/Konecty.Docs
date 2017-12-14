# Authentication

## Token

Ao criar um usuário dentro do konecty e realizar seu primeiro acesso, o sistema gera o Token dentro do banco.
O mesmo pode ser verificado na Collection 'Users'.
Exemplo:

```
{
    "_id" : "4ffcf8108123ddaff50fd05",
    "username" : "admin",
    ...
    "services" : {
        ...
        "resume" : {
            "loginTokens" : [ 
                {
                    "when" : ISODate("2017-12-12T14:20:12.123Z"),
                    "hashedToken" : "PA1ar0VBR/35HY-cwB+9ybQTLklUQIxM6fFoZcB3pyC="
                }
            ]
        }
    }
}
```


## Requisições REST

Para realizar qualquer requisição na API REST do konecty, deve ser primeiro requisitado o token no método de autenticação e o mesmo ser enviado em todas as outras posteriores.

Exemplo de requisição de Token de autenticação.

Realizando um POST para Url ```https://[domain]/rest/auth/login``` com o Header ```"Access-Control-Allow-Origin: *"``` , ```"Content-Type: application/json"``` e os parametros

``` 
{
    "user": "_LOGIN_",
    "password_SHA256": "_PASSWORD_SHA_256_",
    "ns": "[NAMESPACE]"
}
```

Será retornado o seguinte:

```
{
    "success": true,
    "logged": true,
    "authId": "abcdefghijklmnopqrstuvwxyz=",
    "user": (...)
}
```

## Próximas Requisições

Para todas as requisições que necessitarem de autenticação, deve se passar o Token ou via Header ou Cookie.

Exemplo:

```
headers:{
    'Cookie': "_authToken=_AUTH_ID_; _authTokenNs=NOME_DA_EMPRESA",
    'Access-Control-Allow-Origin: *',
	'Content-Type: application/json'
}

```

Ou por exemplo, buscar a lista de produtos via curl:

```
curl -G https://[domain]/rest/data/Product/find --cookie "authTokenId=_AUTH_ID_" -d'
```