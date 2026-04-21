# Design Simples (XP)

## Análise do backend

O código do backend do ESM Forum segue parcialmente o princípio de design simples (YAGNI), pois implementa apenas as funcionalidades necessárias para o funcionamento do sistema de fórum.

## Pontos positivos

- O código não implementa funcionalidades desnecessárias ou excessivamente complexas
- As rotas são diretas e focadas em suas responsabilidades principais
- Uso de SQLite simplifica a persistência de dados

## Possíveis melhorias

- Separação mais clara entre lógica de negócio e rotas (camadas mais bem definidas)
- Modularização maior de funções repetidas
- Melhor organização entre responsabilidades de leitura e escrita de dados

## Conclusão

O sistema segue uma abordagem simples e funcional, adequada ao objetivo.