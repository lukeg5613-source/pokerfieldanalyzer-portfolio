# Decisões de produto e desenvolvimento com IA

## Estatística precisa de denominador

O projeto distingue eventos, oportunidades e mãos únicas. Frequências são acompanhadas de tamanho de amostra e contexto. Isso permite investigar o que uma métrica representa antes de interpretá-la como padrão de comportamento.

## Processar apenas o que mudou

O índice incremental reutiliza as definições estatísticas e compara o conjunto de mãos com um checkpoint compatível. O marco M13.1.1 documenta testes de equivalência com o processamento completo. A abordagem reduz trabalho repetido, mas a estratégia de cópia segura continua tendo custo proporcional ao tamanho do índice.

## Integrar um motor especializado

O marco M14 registra comparação de viabilidade de motores, seleção de um backend executável e integração com limites de recursos. O projeto atua na tradução dos dados, execução controlada e apresentação dos resultados. O motor externo mantém sua autoria e licença próprias.

## Usar agentes sem confundir cálculo e geração

Codex e Kiro são as principais ferramentas de desenvolvimento assistido declaradas pelo autor para o conjunto dos projetos. O histórico local contém marcos com diagnóstico, implementação, regressões e aceitação visual. Não existe uma atribuição auditada de cada mudança a uma ferramenta.

O exemplo mais relevante é a evolução de uma ferramenta de estatísticas para um fluxo de revisão, índices incrementais e integração externa, preservando as definições existentes. IA ajudou no processo de construção; os resultados estatísticos e do solver continuam sujeitos a contratos e verificações explícitas.

## Trade-offs

- SQLite simplifica operação local; cópias de índices grandes podem limitar a atualização.
- Regras explícitas facilitam auditoria; ampliam o trabalho de cobrir casos de domínio.
- Solvers especializados oferecem cálculo de estratégia, mas dependem de premissas e recursos.
- A biblioteca evita recomputação somente quando os parâmetros correspondem corretamente.

O caso demonstra produto orientado por dados, investigação de erros e integração pragmática de componentes.
