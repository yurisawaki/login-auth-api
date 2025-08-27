# Login-Auth-API

## 📌 Sobre o Projeto

Este projeto é uma API de autenticação e autorização desenvolvida em **Java** utilizando **Spring Boot**, **Spring Security** e **JWT (JSON Web Token)**. O objetivo é fornecer um sistema seguro de login e gerenciamento de usuários.

## 🛠️ Tecnologias Utilizadas

- **Java 17**
- **Spring Boot 3**
- **Spring Security**
- **JWT (JSON Web Token)**
- **JPA/Hibernate**
- **Banco de Dados em memória H2**
- **Maven**

## 🚀 Funcionalidades

- Registro de usuários com criptografia de senha (**BCrypt**)
- Login e geração de token JWT
- Validação e refresh do token JWT
- Proteção de rotas com autorização baseada em roles
- Logout e invalidação de token

## 📂 Estrutura do Projeto

```
/login-auth-api
│── src/main/java/com/example/auth
│   ├── controllers
│   ├── dto
│   ├── domain/user
│   ├── repositories
│   ├── infra/security
│   ├── LoginAuthApiApplication.java
│── src/main/resources
│   ├── application.properties
│── pom.xml
```

## 🏗️ Configuração e Execução

### 🔧 Pré-requisitos

Antes de rodar o projeto, você precisa ter instalado:

- [Java 17+](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [Maven](https://maven.apache.org/download.cgi)



### 🏃‍♂️ Rodando o projeto localmente

1. Clone o repositório:

   ```bash
   git clone https://github.com/yurisawaki/login-auth-api.git
   ```

2. Acesse o diretório do projeto:

   ```bash
   cd login-auth-api
   ```

3. Configure o **application.properties**:

   ```bash
   spring.application.name=login-auth-api
   spring.datasource.url=jdbc:h2:mem:testdb
   spring.datasource.driver-class-name=org.h2.Driver
   spring.datasource.username=sa
   spring.datasource.password=
   api.security.token.secret=minha-chave-secreta
   ```

4. Compile e execute o projeto\:mvn spring-boot\:run



### 🔑 Endpoints Principais

| Método | Endpoint         | Descrição                     |
| ------ | ---------------- | ----------------------------- |
| POST   | `/auth/register` | Registro de um novo usuário   |
| POST   | `/auth/login`    | Autenticação e geração de JWT |
| GET    | `/user`          | Perfil do usuário (Protegido) |

## 🔒 Segurança e Autorização

A API utiliza **Spring Security** para autenticação baseada em **JWT**. Apenas usuários autenticados podem acessar rotas protegidas.

## 📜 Licença

Este projeto é distribuído sob a licença MIT. Sinta-se à vontade para usar e modificar! 🚀

