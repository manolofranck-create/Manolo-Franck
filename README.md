# Football Management Simulator

Projeto comunitário de simulador de gerenciamento de futebol inspirado no gênero de Football Manager e FIFA Manager 13, com identidade e implementação próprias.

**Início oficial do projeto: 16/10/2026.**

**Primeira frente de desenvolvimento:** Editor de Dados externo para Windows.

**Estado:** planejamento técnico. Nenhum módulo de software foi implementado ainda.

## Objetivo
Construir um jogo de gestão de futebol em **Unity (C#)**, começando por um **Editor de Dados externo** para Windows. O editor cadastra e valida dados, publica um banco versionado e a Unity usa os dados publicados para iniciar carreiras.

## Primeira entrega: Editor externo
- Interface desktop: Avalonia UI, C# e padrão MVVM.
- Persistência: SQLite, com EF Core e migrations.
- Módulos iniciais, nesta ordem: Países, Cidades, Clubes e Jogadores.
- Dados-base separados dos saves das carreiras.
- Arquitetura modular, testes automatizados e integração futura com Unity.

## Documentação
- [Roadmap](ROADMAP.md)
- [Arquitetura](docs/ARCHITECTURE.md)
- [Banco de dados](docs/DATABASE.md)
- [Decisões e pendências](docs/DECISIONS.md)
- [Contribuição](CONTRIBUTING.md)
- [Histórico](CHANGELOG.md)

Acompanhe e discuta as tarefas em **Issues**. Recursos inspirados em outros jogos não implicam afiliação ou uso de suas marcas e conteúdos protegidos.
