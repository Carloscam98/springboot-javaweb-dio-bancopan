# ![DevSuperior logo](https://raw.githubusercontent.com/devsuperior/bds-assets/main/ds/devsuperior-logo-small.png) Projeto Java Web no Spring Boot 

## Realização
[Carlos Morato ](https://www.linkedin.com/in/carlosamorato/)

### Pré-requisitos

- Lógica de programação java
- Programação orientada a objetos 
- Ferramentas
  - Spring Tool Suite (STS)
  - Postman

### Descrição do projeto

- Resgatar fundamentos de programação
- Colocar em prática esses fundamentos
- Criar um pequeno sistema com ferramentas e práticas de mercado
- Dar mais um passo em direção à preparação para o mercado

### Visão geral do sistema

Sistema (API REST) de usuários e departamentos de uma agência bancária, com os seguintes casos de uso:

- Buscar todos usuários
- Buscar um usuário pelo seu id
- Inserir um novo usuário

### Exemplo do modelo de domínio:
![Image](https://raw.githubusercontent.com/devsuperior/java-web-spring-2022/main/img/dominio.png "Modelo conceitual")

 Desenvolvimento moderno: relacional -> objeto -> json

![Image](https://raw.githubusercontent.com/devsuperior/java-web-spring-2022/main/img/objetos.png "Objetos")

### Passos da aula

- Criar o projeto
- Implementar o modelo de domínio
- Mapeamento objeto-relacional com JPA
- Configurar o banco de dados H2
- Criar os endpoints da API REST

### Trechos de código para copiar

#### Configuração do Maven Resources Plugin

```xml
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-resources-plugin</artifactId>
	<version>3.1.0</version>
</plugin>
```

#### Configurações do banco de dados

```
# Dados de conexão com o banco H2
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

# Configuração do cliente web do banco H2
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

# Configuração para mostrar o SQL no console
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

#### Script SQL

```sql

INSERT INTO tb_department(name) VALUES ('Financeiro');
INSERT INTO tb_department(name) VALUES ('Tecnologia e Operações');

INSERT INTO tb_user(department_id, name, email) VALUES (1, 'Salluan', 'salluanpereira@gmail.com');
INSERT INTO tb_user(department_id, name, email) VALUES (1, 'Bianca', 'bia_somtri@gmail.com');
INSERT INTO tb_user(department_id, name, email) VALUES (2, 'Carlos', 'morato.acarlos@gmail.com');
INSERT INTO tb_user(department_id, name, email) VALUES (2, 'Matheus', 'math.eus@gmail.com');
```
#### Inspiração do projeto

https://www.youtube.com/watch?v=D4frmIHAxEY&ab_channel=DevSuperior


