# Evidências e limites — PokerFieldAnalyzer

Revisão estática em **28/10/2026**, sem abrir bancos, executar solver, importar históricos ou reexecutar testes.

## Resultados históricos

| Marco | Evidência | Interpretação correta |
|---|---|---|
| M14, 03/10/2026 | 127.244 mãos, 104.094 entradas históricas e 3.637.480 eventos de análise agregada | Volumes distintos; eventos não equivalem a usuários ou mãos únicas |
| M14 | 405 testes aprovados e 1 integração opcional ignorada | Resultado histórico de desenvolvimento, não garantia da instalação atual |
| M14 | Primeiro caso real resolvido pelo motor local e biblioteca preenchida | Validação inicial de integração; não cobertura completa de decisões |
| M13.1.1 | Delta de +200 / +2.000 / +10.000 mãos: 5,88 / 11,32 / 46,98 s | Cópias isoladas e fixtures repetidas; inclui preparação/verificação do índice |
| M13.1.1 | Zero divergências entre full e incremental no conjunto isolado | Verificação de equivalência dos casos exercitados; não prova de todos os dados possíveis |

O relatório M13.1.1 registra 439,5 s para um rebuild anterior de aproximadamente 127 mil mãos. Esse processamento tem escopo diferente dos deltas; não se calcula um fator universal de aceleração dividindo os dois tempos.

## Funcionalidades verificadas no código

Parser GGPoker, importação, motores das quatro streets, índices, API, jobs de solver, adaptador postflop e armazenamento de soluções estão presentes. O parser auditado é GGPoker; estruturas para outros formatos não comprovam suporte validado a outras redes.

## Limites do solver

O backend externo documentado é ucsandman/postflop. A execução inicial usou ranges assumidos, árvore finita e rake zero. Resultados são aproximações condicionadas a essas premissas. Não comprovam a melhor ação em qualquer contexto nem vantagem financeira. O uso descrito é estudo local fora do jogo.

## Imagem

Dashboard histórico 7.1 com 81.411 mãos no recorte exibido. A captura contém apenas estatísticas agregadas e foi revisada visualmente. Não expõe histórico de uma mão, identificação de jogador, credencial ou URL de operação. Os pixels foram preservados em PNG sem metadados opcionais.

## Não medido

Não há evidência apresentada de aumento de lucro, melhoria de win rate atribuível ao software, usuários ativos, receita, cobertura GTO integral ou operação em tempo real. Os documentos e as bases originais não são distribuídos.
