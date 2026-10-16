# Sistema de atributos dos jogadores — v1

**Decisão de design:** 36 atributos, cada um com valor inteiro de **0 a 20**. O **Overall (OVR) será definido e implementado posteriormente**; não deve ser calculado como média simples nesta fase.

## Técnicos (12)
1. Finalização
2. Passe curto
3. Passe longo
4. Drible
5. Primeiro toque
6. Cruzamento
7. Cabeceio
8. Desarme
9. Marcação
10. Controle de bola
11. Bolas paradas
12. Pênaltis

## Mentais (10)
1. Visão de jogo
2. Tomada de decisão
3. Concentração
4. Antecipação
5. Posicionamento
6. Criatividade
7. Determinação
8. Trabalho em equipe
9. Liderança
10. Frieza

## Físicos (8)
1. Velocidade
2. Aceleração
3. Agilidade
4. Equilíbrio
5. Força
6. Resistência
7. Impulsão
8. Recuperação física

## Goleiros (6)
1. Reflexos
2. Defesa de chutes
3. Saída do gol
4. Jogo aéreo
5. Reposição de bola
6. Um contra um

## Regras do Editor
- Valores inteiros inclusivos de 0 a 20; impedir valores fora desse intervalo.
- Cada jogador terá os 36 atributos; atributos de goleiro poderão ser apresentados em aba própria.
- Armazenar definições de atributos em catálogo (por exemplo, `AttributeDefinitions`) e valores em `PlayerAttributes`, com chave composta ou unicidade por jogador + atributo.
- Os 36 atributos constituem o conjunto inicial fechado para balanceamento; mudanças futuras deverão ser versionadas e migradas.
- Separar CurrentAbility e PotentialAbility (conceitos de evolução) dos 36 atributos individuais; a escala dessas métricas continua pendente de revisão.
- Não criar Overall/OVR, ranking geral nem fórmula provisória nesta fase.
- Futuramente o Overall poderá usar pesos por posição, mas fórmula, escala e apresentação ainda serão decididas.

## Pendências de design
- Definição operacional de cada atributo no motor de partidas.
- Efeito de atributos físicos e mentais ao longo da carreira.
- Se recuperação física representa característica permanente ou taxa dinâmica.
- Pesos por posição e metodologia de cálculo de Overall.
