# HextechBank - User Service

Microsserviço de gerenciamento de usuários para o projeto do banco digital **HextechBank**.  
Este serviço é responsável por todas as operações relacionadas a usuários, incluindo criação, consulta, atualização e exclusão (CRUD).

---

## 🚀 Tecnologias Utilizadas

- **Java 17**: Versão do Java Development Kit (JDK).
- **Spring Boot 3**: Framework principal para a construção da aplicação.
- **Spring Data JPA**: Camada de persistência para interação com o banco de dados.
- **Maven**: Gerenciador de dependências e build do projeto.
- **H2 Database**: Banco de dados em memória utilizado para o ambiente de desenvolvimento.
- **Lombok**: Biblioteca para reduzir código boilerplate (getters, setters, construtores).

---

## ⚙️ Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/GabrielMiranda05/hextechbank-user-service.git
```

### 2. Navegue até o diretório do projeto
```bash
cd hextechbank-user-service
```
### 3. Execute a aplicação
```bash
mvn spring-boot:run

```
A aplicação estará disponível em:
👉 http://localhost:8080

## Endpoints da API

A seguir estão os endpoints disponíveis neste serviço.

### Criar Usuário

- **URL:** `/users`
- **Método:** `POST`
- **Corpo da Requisição (Request Body):**
  ```json
  {
      "firstName": "string",
      "lastName": "string",
      "document": "string",
      "email": "string",
      "password": "string"
  }
  ```
- **Resposta de Sucesso (Success Response):** `200 OK`

   ### Listar Todos os Usuários
- **URL:** `/users`
- **Método:** `GET`
- **Resposta de Sucesso:** `200 OK`

  ### Buscar Usuário por ID
- **URL:** `/users/{id}`
- **Método:** `GET`
- **Resposta de Sucesso:** `200 OK`
- **Resposta de Erro (se não encontrado):** `404 Not Found`

  ### Atualizar Usuário
- **URL:** `/users/{id}`
- **Método:** `PUT`
- **Corpo da Requisição (Request Body):**
  ```json
  {
      "firstName": "string",
      "lastName": "string",
      "document": "string",
      "email": "string",
      "password": "string"
  }
   ```
  - **Resposta de Sucesso:** `200 OK`
  - **Resposta de Erro (se não encontrado:** `404 Not Found`
 
   ### Deletar Usuário
- **URL:** `/users/{id}`
- **Método:** `DELETE`
- **Resposta de Sucesso:** `204 No Content`
- **Resposta de Erro (se não encontrado):** `404 Not Found`
