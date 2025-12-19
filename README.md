# BookStore API - Spring Data JPA 📚

Este projeto é uma API REST desenvolvida para o gerenciamento de uma livraria, com foco no estudo prático de mapeamentos e relacionamentos complexos utilizando o **Spring Data JPA**.

## 🚀 Tecnologias Utilizadas

* **Java 21**
* **Spring Boot 4**
* **Spring Data JPA**
* **PostgreSQL**
* **Maven**

## 📊 Modelo de Dados e Relacionamentos

A aplicação foi estruturada para demonstrar os principais tipos de associações em bancos de dados relacionais:



1. **Many-to-One / One-to-Many**: Relacionamento entre Livro (`BookModel`) e Editora (`PublisherModel`).
2. **Many-to-Many**: Relacionamento entre Livro (`BookModel`) e Autor (`AuthorModel`), com a criação da tabela intermediária `tb_book_author`.
3. **One-to-One**: Relacionamento entre Livro (`BookModel`) e sua análise (`ReviewModel`).

### Diferenciais Técnicos
* **Identificadores UUID**: Utilização de chaves primárias universais para maior segurança.
* **Controle de Recursão**: Uso de `@JsonProperty(access = JsonProperty.Access.WRITE_ONLY)` para evitar loops infinitos na serialização JSON.
* **Cascade**: Gerenciamento automático de persistência no relacionamento um-para-um.

## 🛠️ Dependências do Projeto

As seguintes dependências foram configuradas no `pom.xml`:

- spring-boot-starter-data-jpa
- spring-boot-starter-webmvc
- postgresql (runtime)

## 🏁 Como Executar

1. Clone o repositório:
   git clone https://github.com/seu-usuario/nome-do-projeto.git

2. Configure suas credenciais do PostgreSQL no arquivo `src/main/resources/application.properties`:
   spring.datasource.url=jdbc:postgresql://localhost:5432/nome_do_banco
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update

3. Execute a aplicação via Maven:
   mvn spring-boot:run

## 📜 Créditos

Este projeto foi desenvolvido com base no excelente material didático da **Micheli Brito**. O conteúdo foi fundamental para o aprendizado de mapeamento de entidades, gerenciamento de associações e boas práticas com Spring Boot e JPA.

---
**Desenvolvido por [Alcides Neto]** 🚀
