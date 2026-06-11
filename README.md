# 🛠️ Autofix - Sistema de Gestão de Oficinas Mecânicas

<p align="center">
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Hibernate%20%2F%20JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white" alt="Hibernate" />
</p>

## 📋 Sobre o Projeto

O **Autofix** é uma plataforma computacional desenvolvida como parte da disciplina de **Projeto de Software** na **PUC Minas**. O sistema foi projetado para automatizar e otimizar toda a esteira operacional e administrativa de uma oficina mecânica, cobrindo desde a jornada inicial do cliente até a retaguarda fiscal e de inventário.

### 🌟 Principais Funcionalidades

- **Módulo de Acesso:** Controle de perfis (Clientes, Secretários, Mecânicos e Gerentes) com autenticação segura via JWT.
- **Módulo de Atendimento:** Auto-cadastro de veículos por clientes e solicitação de agendamentos online triados pela recepção.
- **Módulo de Oficina:** Registro detalhado de diagnósticos, cálculo automatizado de orçamentos (horas trabalhadas + peças) e controle fino do ciclo de vida das Ordens de Serviço (O.S.).
- **Módulo de Retaguarda:** Atualização automatizada de estoque (baixa física de insumos na conclusão de serviços) e simulação de faturamento.

---

## 🏗️ Arquitetura e Tecnologias

O sistema adota uma arquitetura cliente-servidor com separação clara de responsabilidades:

- **Frontend:** SPA desenvolvida em **React** (utilizando componentes modernos e design responsivo).
- **Backend:** API RESTful robusta construída em **Java com Spring Boot**, estruturada em camadas (*Controller*, *Service*, *Repository*).
- **Persistência & ORM:** Banco de dados relacional **PostgreSQL**, utilizando **Hibernate/JPA** com estratégia de herança `JOINED` para mapeamento polimórfico de usuários.

---

## 🚀 Como Executar o Projeto

### Pró-requisitos
Antes de começar, você vai precisar ter instalado em sua máquina:
- [JDK 17](https://www.oracle.com/java/technologies/downloads/) ou superior.
- [Node.js](https://nodejs.org/) (versão LTS).
- [PostgreSQL](https://www.postgresql.org/) ativo na porta padrão (`5432`).
- [Maven](https://maven.apache.org/) para gerenciamento de dependências Java.

### 1. Configuração do Banco de Dados
Crie um banco de dados vazio no PostgreSQL chamado `autofix`. No arquivo do backend (`src/main/resources/application.properties`), ajuste as credenciais de acesso se necessário:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/autofix
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
