Este é um projeto de uma API RESTful desenvolvida com Spring Boot, que simula o backend de uma loja virtual. A aplicação permite o gerenciamento de produtos e categorias, com operações de listagem, criação, atualização e exclusão.

- Tecnologias utilizadas:
  Java 17+
Spring Boot
Spring Data JPA
MariaDB
Maven

Como executar o projeto:
Clone o repositório (ou extraia o .zip):
git clone https://github.com/seu-usuario/seu-repositorio.git

Configure certificando que o MariaDB está rodando e crie um banco de dados chamado 'kaique':
CREATE DATABASE kaique;

Atualize o application.properties (caso necessário):
css
src/main/resources/application.properties
properties
spring.datasource.url=jdbc:mariadb://localhost:3306/kaique
spring.datasource.username=root
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MariaDBDialect
Execute a aplicação:

No terminal:
./mvnw spring-boot:run
Ou use sua IDE (VS Code, IntelliJ, etc.) para iniciar a classe LojaApplication.java.

Endpoints disponíveis:
Produtos:
Método	Endpoint	Descrição
GET	/produtos	Lista todos os produtos
POST	/produtos	Cria um novo produto
PUT	/produtos/{id}	Atualiza um produto
DELETE	/produtos/{id}	Remove um produto

Categorias:
Método	Endpoint	Descrição
GET	/categorias	Lista todas as categorias
POST	/categorias	Cria uma nova categoria
PUT	/categorias/{id}	Atualiza uma categoria
DELETE	/categorias/{id}	Remove uma categoria

Estrutura do projeto:
css
projeto-loja-completo/
├── src/
│   └── main/
│       ├── java/com/example/loja/
│       │   ├── controller/
│       │   ├── model/
│       │   ├── repository/
│       │   └── LojaApplication.java
│       └── resources/
│           └── application.properties
└── pom.xml
