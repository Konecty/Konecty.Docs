# Find

## Descrição

Busca de dados para o `:document`.

Para realizar esta requisição deve-se passar o Token de autenticação.

## Detalhes
```
https://[dominio.konecty]/rest/data/:document/find
```

### Parâmetros

| Parametro |                  Detalhes                  |
|-----------|:------------------------------------------:|
| :document | Representa o sucesso da requisição         |


### Filtros

Passando um objeto na corpo da requisição com o seguinte exemplo:

```
filter={
        "match":"and",
        "conditions":[
            {
                "term":"status",
                "operator":"equals",
                "value":"Ativo"
            }
        ]
    }
```

Propriedade `match` pode receber os seguintes valores:
 - and
 - or

Propriedade `conditions` recebe um array de objetos com propriedades de `term`,`operator` e `value`.

`term` o campo a ser comparado

`operator` pode receber os seguintes valores:

 - equals
 - not equals
 - starts with
 - end with
 - contains
 - not contains
 - less than
 - greater than
 - less or equals
 - greater or equals
 - between
 - equals logged user
 - not equals logged user
 - equals group of logged user
 - not equals group of logged user
 - equals groups of logged user
 - in
 - not in
 - exists

`value` configura o valor a ser utilizado.


## Retorno

Um JSON será o retorno da requisição com os dados:

| Propriedade    | Tipo    |                  Detalhes                                            |
|----------------|---------|:--------------------------------------------------------------------:|
| success        | Boolean | Representa o sucesso da requisição                                   |
| data           | Array   | Lista de objetos com os dados requisitados                           |
| total          | integer | Quantidade de dados retornados                                       |
| errors         | Array   | Lista de objetos com uma propriedade message, para mensagens de erro |

Exemplo de sucesso:
```
{
	"success": true,
	"data": [ (...) ],
	"total": 506
}
```
