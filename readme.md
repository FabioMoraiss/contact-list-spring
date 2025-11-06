# 📞 Contact List

> API de contatos desenvolvida em Java com Spring Boot, seguindo a arquitetura em 3 camadas.


## 🗂️ Arquitetura das Camadas

- **Controller**
  - Responsável pelos endpoints da API e suas configurações (POST, GET, PUT, DELETE e parâmetros).
- **Service**
  - Centraliza as regras de negócio.
- **Repository**
  - Conexão e queries no banco de dados.


## 🚀 Tecnologias Utilizadas

- **Java**
- **Spring Boot**
  - Spring Web
  - Spring JPA
- **Maven**
- **Banco de Dados:** H2 (relacional e em memória)


## 📌 Boas Práticas

- Princípios **SOLID**
- API **RESTful**
- Injeção de Dependências
- Arquitetura em **3 Camadas**


## 📚 Documentação e Endpoints

Acesse a documentação interativa [Swagger UI](http://localhost:8080/swagger-ui/index.html) após fazer build e rodar o projeto.

### 🔹 Criar Contato

```http
POST /contacts
```
```json
{
  "name": "nome de exemplo",
  "phone": "99 99999-9999"
}
```


### 🔹 Buscar Contato por ID

```http
GET /contacts/{id}
```


### 🔹 Atualizar Contato

```http
PUT /contacts
```
```json
{
  "id": 5,
  "name": "nome exemplo",
  "phone": "99 99999-9999"
}
```


### 🔹 Deletar Contato

```http
DELETE /contacts/{id}
```


### 🔹 Listar Contatos por Nome

```http
GET /contacts?name=nome exemplo
```


### 🔹 Listar Todos os Contatos

```http
GET /contacts/all
```

### 🔹 Criar Contatos em Lote

```http
POST /contacts/batch
```
```json
[
  {
    "name": "nome exemplo",
    "phone": "99 99999-9999"
  },
  {
    "name": "nome exemplo 2",
    "phone": "88 88888-8888"
  }
]
```


### 🔹 Deletar Contatos em Lote

```http
DELETE /contacts/delete-batch
```
```json
[1, 2, 3]
```


## 💡 Observações

- Todas as requisições devem ser feitas para `http://localhost:8080`.
- Utilize o Swagger para testar e explorar os endpoints disponíveis.
