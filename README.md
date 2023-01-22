# Gerenciador de tarefas

### DIO - Trilha .NET - API e Entity Framework
www.dio.me

## Desafio de projeto

Construir um sistema gerenciador de tarefas, onde pode-se cadastrar uma lista de tarefas que permitirá organizar melhor uma rotina.

Essa lista de tarefas tem um CRUD, ou seja, permite obter os registros, criar, salvar e deletar esses registros.

Esta aplicação é do tipo Web API.

A classe principal, a classe de tarefa, é a seguinte:

![Diagrama da classe Tarefa](diagrama.png)


## Métodos disponíveis
Os métodos disponiveis são indicados a seguir:


**Swagger**


![Métodos Swagger](swagger.png)


**Endpoints**


| Verbo  | Endpoint                | Parâmetro | Body          |
|--------|-------------------------|-----------|---------------|
| GET    | /Tarefa/{id}            | id        | N/A           |
| PUT    | /Tarefa/{id}            | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}            | id        | N/A           |
| GET    | /Tarefa/ObterTodos      | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo  | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData    | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus  | status    | N/A           |
| POST   | /Tarefa                 | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```

