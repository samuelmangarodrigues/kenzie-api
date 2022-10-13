# TesteTecnicoKenzie
Teste técnico Kenzie Academy Brazil.
Essa aplicação permite criar tarefas, completar tarefas, editar e excluir.\
Aplicação feita em Django(Python).

## Bibliotecas utilizadas:
### asgiref==3.5.2
### black==22.10.0
### certifi==2022.9.24
### charset-normalizer==2.1.1
### click==8.1.3
### colorama==0.4.5
### dj-database-url==1.0.0
### django-cors-headers==3.13.0
### django-heroku==0.3.1
### django-rest-framework==0.1.0
### gunicorn==20.1.0
### heroku==0.1.4
### idna==3.4
### mypy-extensions==0.4.3
### pathspec==0.10.1
### platformdirs==2.5.2
### psycopg2==2.9.4
### python-dateutil==1.5
### pytz==2022.4
### requests==2.28.1
### six==1.16.0
### sqlparse==0.4.3
### tomli==2.0.1
### tzdata==2022.5
### urllib3==1.26.12
### whitenoise==6.2.0

## EndPoints

## Todo

## Post | Todo

`https://test-kenzie.herokuapp.com/api/todo/`

O usuário deve passar a descrição da tarefa e receberá um status 201 CREATED

`Requisição `

```json
{
  "description": "Tomar água",
}
```

`Resposta | 201 CREATED`


```json
{
	"id": 3,
	"description": "tomar água",
	"completed": false
}

```

## Get | Todo

`https://test-kenzie.herokuapp.com/api/todo/`

Requisição para listar as tarefas.

`Requisição `

> Não tem corpo na requisição.

`Resposta | status 200 OK`

Retorna uma lista com todas as tasks criadas, status 200 OK.

```json
[
	{
		"id": 3,
		"description": "tomar água",
		"completed": false
	},
	{
		"id": 4,
		"description": "comprar cerveja",
		"completed": false
	},
	{
		"id": 5,
		"description": "beber remédio",
		"completed": false
	}
]
```
## Get | Todo

`https://test-kenzie.herokuapp.com/api/todo/3`

O usuário deve passar o id para listar a tarefa específica.

`Requisição `

> Não tem corpo na requisição.

`Resposta | status 200 OK`

Retorna a tarefa específica de acordo com o Id da task, status 200 OK.

```json
{
	"id": 3,
	"description": "tomar água",
	"completed": false
}
```

## Put | Todo

`https://test-kenzie.herokuapp.com/api/todo/3/`

O usuário deve passar o id da task para completa-lá, status 200 OK.

`Requisição `

> Sem corpo na requisição

`Resposta | 200 OK`

Atualiza a chave completed, colocando-a como true.

```json
{
	"id": 3,
	"description": "tomar água",
	"completed": true
}

```


## Patch | Todo

`https://test-kenzie.herokuapp.com/api/todo/3/`

O usuário deve passar o id da task e a nova descrição da tarefa, status 200 OK.

`Requisição `

```json
{
	"description":"tomar café"
}
```

`Resposta | 200 OK`

```json
{
	"id": 3,
	"description": "tomar café",
	"completed": true
}

```

## Delete | Todo

`https://test-kenzie.herokuapp.com/api/todo/3/`

O usuário deve passar o id da task para deleta-lá, status 200 OK.

`Requisição `

> Sem corpo na requisição

`Resposta | 200 OK`

```json
{
	"message":"deleted"
}

```
