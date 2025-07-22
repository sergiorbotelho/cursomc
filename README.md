# Estudo de Caso Java com Spring Boot e JPA

Este repositório contém a implementação prática de um modelo conceitual orientado a objetos utilizando **Java**, **Spring Boot** e **JPA**. O projeto foi desenvolvido com base no curso ["Modelagem Conceitual com Diagrama de Classes da UML"](https://www.udemy.com/user/nelio-alves), ministrado pelo Prof. Dr. Nelio Alves.

## 🎯 Objetivo

Demonstrar como implementar um modelo conceitual utilizando boas práticas de mercado com **Java + Spring Boot**, abordando:

- Leitura e interpretação de diagramas de classes e objetos
- Relacionamentos: 1:N, N:1, 1:1, N:N
- Classes de associação, herança e enumerações
- Entidades fracas com `@ElementCollection`
- API REST para exposição dos dados

<img width="1418" height="794" alt="image" src="https://github.com/user-attachments/assets/66b39032-52b8-41b8-ac97-7b64add1b753" />

<img width="1761" height="681" alt="image" src="https://github.com/user-attachments/assets/a0040573-9e07-4feb-9027-54f216dcf64c" />

## 📚 Tecnologias Utilizadas

- Java 8
- Spring Boot (1.5.x ou 2.x.x)
- Spring Data JPA
- H2 Database (banco em memória)
- Maven
- Postman
- Git/GitHub
- Spring Tool Suite (ou Eclipse)

## 🛠️ Instalação e Execução

### Pré-requisitos

- Java JDK 8 (64 bits)
- STS ou Eclipse com suporte a Spring
- Git instalado
- Postman para testar os endpoints

### Passos

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

1. Abra o projeto no STS ou Eclipse  
2. Execute a aplicação: `Run As > Spring Boot App`  
3. Acesse o console H2:  
   - `http://localhost:8080/h2-console`  
   - JDBC URL: `jdbc:h2:mem:testdb`

## 🔗 Endpoints REST Disponíveis

| Método | Endpoint           | Descrição                                         |
|--------|--------------------|--------------------------------------------------|
| GET    | `/categorias/{id}` | Retorna categoria e seus produtos                |
| GET    | `/clientes/{id}`   | Retorna cliente, telefones e endereços          |
| GET    | `/pedidos/{id}`    | Retorna pedido com cliente, pagamento e endereço|

## 📁 Estrutura do Projeto

```
src/
├── main/
│   ├── java/
│   │   └── com/nelioalves/cursomc/
│   │       ├── domain/         # Entidades JPA
│   │       ├── repositories/   # Interfaces JpaRepository
│   │       ├── resources/      # Controladores REST
│   │       ├── services/       # Lógica de negócio
│   │       ├── enums/          # Enums personalizados
│   │       └── exceptions/     # Tratamento de exceções
│   └── resources/
│       └── application.properties
```

## ✅ Funcionalidades

- Modelagem de dados com JPA e Hibernate
- Mapeamento de relacionamentos complexos
- Herança com `@Inheritance(strategy = JOINED)`
- Chave composta com `@EmbeddedId`
- Enumerações com métodos utilitários (`toEnum`)
- Serialização JSON com `@JsonIgnore` para evitar loops
- Tratamento de exceções com `@ControllerAdvice`
- Base de dados gerada e populada automaticamente via Spring Boot

## 👨‍🏫 Créditos

Curso: [Modelagem Conceitual com UML](https://www.udemy.com/user/nelio-alves)  
Instrutor: **Prof. Dr. Nelio Alves**

## 📄 Licença

Projeto desenvolvido exclusivamente para fins educacionais, seguindo os termos de uso da plataforma Udemy e do conteúdo do curso original.
