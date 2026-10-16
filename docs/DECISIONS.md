# Registro de decisões

## Aceitas como direção de projeto
- Iniciar pelo **Editor de Dados externo**, antes do jogo Unity.
- Evoluir modularmente: Países → Cidades → Clubes → Jogadores.
- Editor Windows com **C# + Avalonia UI**, usando padrão MVVM.
- Banco **SQLite** e camada de persistência **EF Core**, com migrations.
- Separar dados-base e saves do jogo; versões publicadas devem ser validadas.
- Documentação e tarefas públicas no GitHub, em português.
- Codex/ChatGPT Work para apoiar implementação, testes e revisão, não para substituir validação.

- Sistema inicial de **36 atributos de jogadores**, inteiros de **0 a 20**: 12 técnicos, 10 mentais, 8 físicos e 6 de goleiro. **Overall fica para uma etapa futura**, sem fórmula provisória. Ver [especificação](PLAYER_ATTRIBUTES.md).

## Propostas a confirmar
- Múltiplos bancos editáveis no Editor (criar, abrir, duplicar, publicar) versus banco principal único. Recomenda-se suporte a múltiplos bancos, mas não houve decisão final.
- Detalhes de licenciamento do repositório e políticas de contribuição.
- Versões de .NET, Avalonia, EF Core e Unity.
- Formato de exportação, contratos de compatibilidade e política de migrações.
- Escopo exato dos modos de carreira (treinador, gestão administrativa, presidente, investidor ou proprietário).

## Prática
Para mudanças arquiteturais importantes, registrar contexto, opções, decisão, consequências e data neste arquivo antes da implementação.
