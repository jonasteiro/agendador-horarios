# 📅 Agendador de Horários

Sistema de agendamento de horários desenvolvido em **Java 25** com **Spring Boot**, com foco em boas práticas de desenvolvimento, organização em camadas e arquitetura limpa. Projeto criado como parte de portfólio, para consolidar conceitos de back-end com Spring.

## ✨ Funcionalidades

- Cadastro de agendamentos
- Listagem de agendamentos
- Consulta de agendamento por ID
- Atualização de agendamentos
- Cancelamento/exclusão de agendamentos
- Validação de dados de entrada

## 🚀 Tecnologias utilizadas

- **Java 25**
- **Spring Boot**
- **Spring Web** (API REST)
- **Spring Data JPA**
- **Maven** (gerenciador de dependências)
- Banco de dados relacional (ex: H2 / MySQL / PostgreSQL — ajustar conforme `application.properties`)

## 🏗️ Arquitetura do projeto

O projeto segue uma organização em camadas, separando responsabilidades:

```
com.joao.agendador_horarios
├── controller
│   └── AgendamentoController      # Camada de entrada (endpoints REST)
├── infrastructure
│   ├── entity
│   │   └── Agendamento            # Entidade JPA
│   └── repository
│       └── AgendamentoRepository  # Acesso a dados (Spring Data JPA)
├── services
│   └── AgendamentoService         # Regras de negócio
└── AgendadorHorariosApplication   # Classe principal (main)
```

Essa separação facilita a manutenção, testes e evolução do projeto, seguindo o princípio de responsabilidade única entre as camadas de apresentação, negócio e persistência.

## 📂 Estrutura de pastas

```
agendador-horarios/
├── .mvn/wrapper/
├── src/
│   ├── main/
│   │   ├── java/com/joao/agendador_horarios/
│   │   └── resources/
│   │       ├── static/
│   │       ├── templates/
│   │       └── application.properties
│   └── test/
├── mvnw
├── mvnw.cmd
└── pom.xml
```

## ⚙️ Pré-requisitos

Antes de rodar o projeto, você precisa ter instalado:

- [Java 25 (JDK)](https://jdk.java.net/25/)
- [Maven](https://maven.apache.org/) (ou utilizar o Maven Wrapper incluso no projeto)
- Uma IDE de sua preferência (IntelliJ, VS Code, Eclipse, etc.)

## ▶️ Como executar o projeto

1. Clone o repositório:
```bash
git clone https://github.com/jonasteiro/agendador-horarios.git
cd agendador-horarios
```

2. Execute o projeto utilizando o Maven Wrapper:
```bash
# Linux/Mac
./mvnw spring-boot:run

# Windows
mvnw.cmd spring-boot:run
```

3. A aplicação estará disponível em:
```
http://localhost:8080
```

## 🔗 Endpoints da API

| Método | Endpoint                  | Descrição                        |
|--------|----------------------------|-----------------------------------|
| GET    | `/agendamentos`            | Lista todos os agendamentos       |
| GET    | `/agendamentos/{id}`       | Busca um agendamento por ID       |
| POST   | `/agendamentos`            | Cria um novo agendamento          |
| PUT    | `/agendamentos/{id}`       | Atualiza um agendamento existente |
| DELETE | `/agendamentos/{id}`       | Remove um agendamento             |

> Ajuste esta tabela conforme os endpoints reais implementados no `AgendamentoController`.

## 🧪 Testes

O projeto conta com uma estrutura de testes em `src/test`, podendo ser executados com:

```bash
./mvnw test
```

## 📌 Melhorias futuras

- [ ] Adicionar autenticação e autorização (Spring Security)
- [ ] Documentação da API com Swagger/OpenAPI
- [ ] Validação de conflitos de horários
- [ ] Interface front-end para consumo da API
- [ ] Testes unitários e de integração mais abrangentes

## 👤 Autor

Desenvolvido por **[jonasteiro](https://github.com/jonasteiro)**.

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para utilizá-lo como referência de estudo.
