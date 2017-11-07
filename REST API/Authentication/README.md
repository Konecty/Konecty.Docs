# Authentication

Exemplo de requisição de Token de autenticação.

Realizando um POST para Url ```https://[domain]/rest/auth/login``` com o Header ```"Content-Type: application/json"``` e os parametros

``` 
{
    "user": "_LOGIN_",
    "password_SHA256": "_PASSWORD_SHA_256_",
    "ns": "[NAMESPACE]"
}
```
