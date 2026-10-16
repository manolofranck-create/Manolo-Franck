# Roadmap público

> Planejamento inicial, sujeito a evolução. **Planejado** não significa implementado.

## Fase 0 — Fundação do Editor (planejado)
- [ ] Organizar solução .NET modular: Desktop, Application, Domain, Infrastructure, DataContracts e Tests.
- [ ] Criar aplicação Avalonia com navegação e MVVM.
- [ ] Configurar SQLite, EF Core, migrations, versionamento de esquema e testes.
- [ ] Definir gerenciador de bancos: criar, abrir, duplicar, backup, validar e publicar. **Escopo de múltiplos bancos ainda em discussão.**

## Fase 1 — Cadastros (planejado)
- [ ] Países: CRUD, ISO2/ISO3, continente, nacionalidade e ativo.
- [ ] Cidades: vínculos com países, pesquisa e validação.
- [ ] Clubes: identificação, localização, reputação, cores e dados econômicos básicos.
- [ ] Jogadores: identificação, nascimento, nacionalidade, posição, habilidade e clube opcional.

## Fase 2 — Publicação e integração (planejado)
- [ ] Validar integridade e publicar banco somente após aprovação.
- [ ] Definir contratos estáveis, versão e compatibilidade do banco.
- [ ] Carregador na Unity e criação de saves separados dos dados-base.

## Fase 3 — Simulador (futuro)
- [ ] Calendário, competições e classificação.
- [ ] Motor de partidas e estatísticas.
- [ ] Contratos, transferências, finanças, IA de clubes e desenvolvimento de jogadores.
- [ ] Interfaces do jogo e, posteriormente, apresentação 2D/3D de partidas.

## Como acompanhar
As [Issues](../../issues) representam entregas verificáveis; use comentários para propor alterações. Atualize o checklist após implementar e testar funcionalidades.
