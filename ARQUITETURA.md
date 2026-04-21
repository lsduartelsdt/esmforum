# Análise Arquitetural do ESM Forum

## Estilo Arquitetural

O sistema ESM Forum segue principalmente o estilo de arquitetura em camadas (Layered Architecture), com uma separação básica entre frontend e backend.

Também apresenta características do padrão cliente-servidor:

- Cliente: aplicação React (frontend)
- Servidor: aplicação Node.js com Express (backend)

---

## Camadas Identificadas

### 1. Camada de Apresentação
Representada pelo frontend em React, responsável pela interface com o usuário.

### 2. Camada de Negócio (parcial)
Presente no server.js, onde estão as regras básicas de funcionamento do sistema.

### 3. Camada de Dados
Representada pelo arquivo modelo.js, responsável pelo acesso ao banco SQLite.

---

## Comunicação entre Frontend e Backend

A comunicação ocorre via HTTP, utilizando requisições REST:

- GET / → listar perguntas
- POST /perguntas → cadastrar pergunta
- GET /respostas/:id → listar respostas
- POST /respostas → cadastrar resposta

---

## Diagrama Arquitetural

```mermaid
flowchart TD
Frontend[Frontend React]
Backend[Backend Node.js (Express)]
Database[(SQLite)]

Frontend --> Backend
Backend --> Database