# Proposta de Organização Arquitetural

## Separação em Camadas

### 1. Camada de Apresentação (Routes)

Responsável por receber requisições HTTP e enviar respostas.

Exemplos:
- server.js
- rotas de perguntas, respostas e votação

---

### 2. Camada de Negócio (Services)

Responsável pelas regras de negócio.

Exemplos:
- voteService.js
- lógica de votação
- validações

---

### 3. Camada de Dados (Repository)

Responsável pelo acesso ao banco de dados.

Exemplos:
- modelo.js
- voteRepository.js

---

## Comunicação entre camadas

- Routes chamam Services
- Services chamam Repository
- Repository acessa o banco

---

## Aplicação do Padrão MVC

### Model
- Pergunta
- Resposta
- Voto

Responsável pelos dados e persistência.

---

### Controller
- Rotas do Express (server.js)

Responsável por receber requisições e chamar os serviços.

---

### View
- Respostas JSON retornadas ao frontend

---

## Exemplo de fluxo

1. Usuário envia voto
2. Route recebe requisição
3. Controller chama VoteService
4. Service aplica regra de negócio
5. Repository salva no banco
6. Sistema retorna resposta JSON

---

## Diagrama MVC

```mermaid
flowchart TD
User --> Controller
Controller --> Service
Service --> Repository
Repository --> Database[(DB)]