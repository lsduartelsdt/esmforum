# Análise dos Princípios SOLID no ESM Forum

## Pontos Positivos

### 1. Separação do modelo de dados (SRP)

O arquivo modelo.js é responsável pelas operações relacionadas ao banco de dados, como cadastro e busca de perguntas e respostas.

Isso segue o princípio SRP (Single Responsibility Principle), pois concentra a responsabilidade de acesso aos dados em um único módulo.

---

### 2. Uso de funções específicas para cada operação (SRP)

As funções no modelo.js, como cadastrar_pergunta, listar_perguntas e cadastrar_resposta, possuem responsabilidades bem definidas.

Cada função executa uma única tarefa, o que facilita manutenção e entendimento do código.

---

### 3. Estrutura modular com require (DIP - parcialmente)

O uso de require para importar módulos demonstra uma separação básica entre arquivos, reduzindo acoplamento direto entre partes do sistema.



---

## Oportunidades de Melhoria

### 1. Violação do SRP no server.js

O arquivo server.js concentra múltiplas responsabilidades:

- Definição de rotas
- Regras de negócio
- Acesso ao modelo

Isso viola o princípio SRP, pois um único arquivo está realizando várias funções diferentes.

**Melhoria proposta:**
Separar em camadas:
- Controllers (rotas)
- Services (lógica de negócio)
- Repositories (acesso a dados)

---

### 2. Violação do DIP (Dependency Inversion Principle)

O server.js - chamado de router no enunciado - depende diretamente do modelo.js, utilizando suas funções sem abstração intermediária.

Isso cria um acoplamento forte entre as camadas.

**Melhoria proposta:**
Introduzir uma camada de serviço (service), como feito na funcionalidade de votação, onde o server chama o service e não diretamente o modelo.

Isso reduz o acoplamento e melhora a flexibilidade do sistema.