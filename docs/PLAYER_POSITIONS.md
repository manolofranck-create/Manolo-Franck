# Posições dos jogadores — v1

**Decisão:** 11 posições oficiais. LD e LE são posições distintas. Posições e familiaridade não fazem parte dos 36 atributos de jogador.

| Código | Nome | Setor |
|---|---|---|
| GOL | Goleiro | Gol |
| ZAG | Zagueiro | Defesa |
| LD | Lateral direito | Defesa |
| LE | Lateral esquerdo | Defesa |
| VOL | Volante / meia defensivo | Meio-campo |
| MC | Meia central | Meio-campo |
| MD | Meia direita | Meio-campo |
| ME | Meia esquerda | Meio-campo |
| PD | Ponta direita | Ataque |
| PE | Ponta esquerda | Ataque |
| ATA | Atacante | Ataque |

## Modelo proposto
- Catálogo `PositionDefinitions` com código estável, nome, setor e ordem de exibição.
- `PlayerPositions`: `PlayerId`, `PositionCode`, `Familiarity` (inteiro de 0 a 20), `IsPrimary`.
- Cada jogador tem exatamente uma posição principal, e pode ter zero ou mais secundárias.
- Não repetir uma mesma posição para o mesmo jogador; unicidade `PlayerId + PositionCode`.
- Não aceitar valores de familiaridade fora do intervalo 0–20.
- A posição principal não deve ser armazenada simultaneamente em outro campo divergente; migrar o campo `Players.Position` de forma segura quando implementar.
- Exemplo ilustrativo: MC principal com familiaridade 20; VOL secundária 15; MD secundária 10.
- Não inferir automaticamente posições a partir de atributos; a escolha é explícita no Editor.

## Interface do Editor
- Seleção obrigatória da posição principal.
- Seleção de posições secundárias sem duplicatas.
- Campo de familiaridade por posição e validação imediata.
- Exibir siglas, nomes completos e setores.
- Persistir alterações de forma atômica; testar criação, edição, exclusão de posição secundária e troca de principal.

## Fora do escopo inicial
- Overall (OVR), pesos por posição e penalidades de atuar fora de posição.
- Formações táticas, papéis/funções específicas, movimentação no campo e motor de partidas.
- Adição de novas posições sem nova decisão de design.

## Ponto a confirmar
A familiaridade de 0–20 é uma **recomendação de implementação**, não uma decisão expressa do usuário. Confirmar antes de implementá-la como regra definitiva.
