# Padrões de Projeto Existentes no ESM Forum

## 1. Padrão MVC (parcial)

O sistema segue parcialmente o padrão MVC:

- Model: representado pelo arquivo modelo.js, responsável pelo acesso aos dados
- Controller: representado pelo server.js, que trata as requisições HTTP
- View: representada pelas respostas JSON enviadas ao frontend

A implementação não está totalmente separada, pois o server.js também contém lógica de negócio.

---

## 2. Padrão Repository (implícito)

O arquivo modelo.js funciona como um repositório de dados, centralizando operações de leitura e escrita no banco.

Isso se aproxima do padrão Repository, embora não esteja formalmente estruturado.

---

## 3. Padrão Layered Architecture (parcial)

O sistema apresenta uma separação básica em camadas:

- Camada de apresentação (server.js)
- Camada de dados (modelo.js)

No entanto, não há uma camada intermediária de negócio bem definida.

---

## Conclusão

Os padrões estão presentes de forma parcial e simplificada, o que é comum em sistemas didáticos. Há oportunidades claras de melhoria com a introdução de camadas mais bem definidas.