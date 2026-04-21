# Caso de Uso: Votar em Pergunta

## Atores
- Usuário autenticado

## Pré-condições
- Usuário está logado
- A pergunta existe no sistema

## Fluxo Principal
1. O sistema exibe lista de perguntas
2. O usuário seleciona uma pergunta
3. O usuário clica em upvote ou downvote
4. O sistema verifica se o usuário já votou
5. O voto é registrado no banco de dados
6. O sistema atualiza o contador de votos
7. O sistema exibe atualização na interface

## Fluxo Alternativo
### Usuário já votou:
4a. Sistema detecta voto existente  
4b. Sistema remove voto anterior  
4c. Sistema registra novo voto  
4d. Retorna ao fluxo principal

## Pós-condições
- O voto é armazenado corretamente
- A pontuação da pergunta é atualizada