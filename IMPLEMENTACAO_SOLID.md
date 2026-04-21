# Implementação com SOLID

## Funcionalidade escolhida
Sistema de votação em perguntas

## Aplicação dos princípios

### SRP
Separação entre:
- server.js (rotas)
- voteService.js (lógica)
- voteRepository.js (dados)

### DIP
O server.js não acessa diretamente o banco, delegando ao service.

### OCP
A lógica pode ser estendida sem modificar o código existente.