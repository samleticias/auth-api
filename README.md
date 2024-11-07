# API de Autenticação

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

Este projeto é uma API construída usando **Java, Spring Boot, PostgreSQL, Flyway Migrations, Spring Security e JWT** para controle de autenticação e autorização de usuários.

## Tecnologias

- [Java](https://www.java.com/)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [PostgreSQL](https://www.postgresql.org/)
- [Spring Security](https://spring.io/projects/spring-security)
- [JWT (JSON Web Token)](https://jwt.io/)
- [Flyway](https://www.baeldung.com/database-migrations-with-flyway)

## Funcionalidades

A API oferece os seguintes endpoints:

- **GET /product**: Retorna uma lista de todos os produtos (acesso para todos os usuários autenticados).
- **POST /product**: Registra um novo produto (acesso restrito a usuários com a permissão de ADMIN).
- **POST /auth/login**: Permite o login na aplicação.
- **POST /auth/register**: Registra um novo usuário na aplicação.

## Autenticação

A autenticação é gerida pelo **Spring Security**, e a API possui os seguintes papéis:

- **USER**: Papel padrão para usuários logados.
- **ADMIN**: Papel com permissões administrativas para gerenciar dados, como o registro de novos produtos.

Para acessar os endpoints protegidos como um usuário ADMIN, é necessário fornecer as credenciais de autenticação no cabeçalho da requisição.
