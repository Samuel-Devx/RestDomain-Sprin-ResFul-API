<div align="center">

<img src="https://img.shields.io/badge/RestDomain-v0.0.1-6366f1?style=for-the-badge&logoColor=white" />
<img src="https://img.shields.io/badge/Status-Concluído-22c55e?style=for-the-badge" />
<img src="https://img.shields.io/badge/Licença-MIT-60a5fa?style=for-the-badge" />
<img src="https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Spring%20Boot-4.0.1-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
<img src="https://img.shields.io/badge/PostgreSQL-Deploy-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />

</div>

---

# ☁️ RestDomain

> API RESTful desenvolvida com Spring Boot e implantada na nuvem — modelagem de domínio bancário com documentação Swagger integrada.

---

## Sobre o Projeto

O **RestDomain** é uma API RESTful construída com **Spring Boot 4**, seguindo boas práticas de modelagem orientada a domínio. O projeto simula o contexto de uma conta bancária digital, expondo endpoints para gerenciamento de usuários, contas, cartões, funcionalidades e notícias.

A API é documentada com **Swagger/OpenAPI**, possui persistência de dados via **PostgreSQL** e está preparada para deploy em nuvem através de um `Procfile`.

---

##  Funcionalidades

- Criação e consulta de usuários
-  Gerenciamento de contas bancárias (saldo e limite)
- Associação de cartão com limite por usuário
- Listagem de funcionalidades disponíveis por usuário
- Exibição de notícias personalizadas por usuário
- Documentação interativa via Swagger UI

---


## Estrutura de Dados

A API retorna os dados do usuário no seguinte formato:

```json
{
  "name": "Samuel Dev",
  "account": {
    "number": "0001-1",
    "agency": "0001",
    "balance": 1500.00,
    "limit": 500.00
  },
  "features": [
    { "icon": "💸", "description": "Transferência" }
  ],
  "card": {
    "number": "**** **** **** 1234",
    "limit": 2000.00
  },
  "news": [
    { "icon": "📢", "description": "Nova atualização disponível" }
  ]
}
```

### Pré-requisitos

- Java >= 17
- Maven >= 3.8
- PostgreSQL >= 14

### Configuração do Banco de Dados

Configure as variáveis de ambiente ou o arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/restdomain
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

---

## 🛠️ Tecnologias Utilizadas

- **Java 17** — Linguagem principal
- **Spring Boot 4.0.1** — Framework para criação da API REST
- **Spring Data JPA** — Persistência e mapeamento objeto-relacional
- **PostgreSQL** — Banco de dados relacional em nuvem
- **SpringDoc OpenAPI 3** — Documentação automática via Swagger UI
- **Maven** — Gerenciamento de dependências e build

---

## 📄 Licença

Este projeto está sob a licença **MIT**. Veja o arquivo [LICENSE](./LICENSE) para mais detalhes.

---

<div align="center">
  Feito por <strong>Samuel-Dev</strong> 🚀
</div
