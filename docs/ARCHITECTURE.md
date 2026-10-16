# Arquitetura planejada

## Princípios
1. Editor **externo** à Unity, independente do runtime e do projeto do jogo.
2. Separação entre interface, casos de uso, domínio, persistência e contratos de dados.
3. **Banco de autoria** (master) distinto da publicação para o jogo e dos saves de carreira.
4. Identificadores estáveis para referenciar entidades; integridade referencial e migrações.
5. Testes de regras de domínio e de persistência sem depender da UI.

## Stack inicial proposta
- C# e Avalonia UI (MVVM) para o editor desktop Windows.
- SQLite e EF Core para persistência do editor.
- xUnit para testes.
- Unity e C# para o jogo, em etapa posterior.

## Projetos pretendidos
```text
Editor/
  Football.Editor.Desktop/
  Football.Editor.Application/
  Football.Editor.Domain/
  Football.Editor.Infrastructure/
  Football.Editor.Tests/
Shared/
  Football.DataContracts/
Database/
  Development/
  Published/
  Backups/
UnityGame/
```

## Fluxo de dados
Editor → banco master SQLite → validações/publicação versionada → leitor no jogo Unity → novo save de carreira independente.

## Segurança e integridade
Publicação deve fazer cópia/artefato validado em vez de disponibilizar edição ao vivo do master para o jogo. Definir estratégia de backups e compatibilidade de versão antes de publicar.
