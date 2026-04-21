# Proposta de Aplicação de Padrões de Projeto

## 1. Strategy Pattern (Sistema de Votação)

### Justificativa
Permite diferentes tipos de votação (upvote, downvote) sem alterar o código principal.

### Solução
Criar estratégias separadas para cada tipo de voto.

### Exemplo de código

```js
class Upvote {
  executar() {
    console.log("Upvote aplicado");
  }
}

class Downvote {
  executar() {
    console.log("Downvote aplicado");
  }
}

---

## Segundo padrão (Observer)

```md id="jd2szr"
## 2. Observer Pattern (Notificações)

### Justificativa
Permite notificar usuários quando novas respostas são adicionadas.

### Solução
Usuários se inscrevem para receber notificações.

### Exemplo

```js
class Notificador {
  notificar() {
    console.log("Usuário notificado");
  }
}


---

## Terceiro padrão (Factory)

```md id="7m0d4u"
## 3. Factory Pattern (Criação de objetos)

### Justificativa
Centraliza a criação de objetos como Pergunta e Resposta.

### Solução

```js
function criarPergunta(texto) {
  return { texto: texto };
}