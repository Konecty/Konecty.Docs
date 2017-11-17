# Find by id

## Descrição

Busca de dados para o `:document` com o `_id` enviado por parametro

Para realizar esta requisição deve-se passar o Token de autenticação.

## Detalhes
```
https://[dominio.konecty]/rest/data/:document/:dataId
```

### Parâmetros

| Parametro |                  Detalhes                  |
|-----------|:------------------------------------------:|
| :document | Representa o sucesso da requisição         |
| :dataId   | Lista de objetos com os dados requisitados |


## Retorno

Um JSON será o retorno da requisição com dados referente ao suce

| Propriedade    | Tipo    |                  Detalhes                                            |
|----------------|---------|:--------------------------------------------------------------------:|
| success        | Boolean | Representa o sucesso da requisição                                   |
| data           | Array   | Lista de objetos com os dados requisitados                           |
| total          | integer | Quantidade de dados retornados                                       |
| errors         | Array   | Lista de objetos com uma propriedade message, para mensagens de erro |


```
{
	"success": true,
	"data": [ (...) ],
	"total": 506
}
```
