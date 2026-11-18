# Registro de uso de IA (prompts.md)

Regra da GS: IA é permitida como copiloto, com prompts registrados, e **todo integrante precisa saber explicar cada linha**. Ferramenta usada: Claude (Anthropic).

| # | Data | Prompt (resumo fiel) | O que a IA entregou | O que o grupo revisou/alterou |
|---|---|---|---|---|
| 1 | 12/11/2026 | Enviamos o PDF do desafio e contamos que o professor ia pedir um projeto sobre ondas de calor, usando como exemplo ações da prefeitura (troca de árvores do calçadão por toldos). Matéria: Inteligência Artificial. | Leitura do PDF e resumo das exigências da disciplina de IA (entregáveis, critérios, regras). | *(preencher)* |
| 2 | 12/11/2026 | "Quero que você faça o trabalho da matéria de IA pra mim e quero tirar 10." | Estrutura do repositório `ml/`, notebook (`citizentech_calor_extremo.ipynb`), template do relatório, `dados/README.md`, `requirements.txt`, roteiro do vídeo. Código primeiro testado com dados sintéticos no ambiente da IA (só para depurar); os resultados finais vêm dos dados reais do INMET (linha 5). | *(preencher)* |
| 3 | 12/11/2026 | "A cidade vai ser Osasco" (com capturas do portal do INMET mostrando a estação São Paulo – Mirante a ~18 km). | Ajuste do projeto para Osasco, mantendo a estação A701 como fonte de dados. | *(preencher)* |
| 4 | 16/11/2026 | "Só 2025 dá para fazer?" | Teste do notebook com 1 ano e com 2022–2025 (em dados sintéticos); recomendou 2022–2025. | *(preencher)* |
| 5 | 16/11/2026 | Enviamos os zips do INMET de 2022 a 2025. | Extraiu os CSV da A701, executou o notebook com os dados reais, conferiu os dados de forma independente (percentil 90 e dia mais quente) e corrigiu os textos automáticos do relatório (overfitting, comparação com a persistência, limitações). | *(preencher)* |
| 6 | 16/11/2026 | "Está com cara de IA o meu trabalho?" | Resposta honesta: sim, em parte; sugestões para o grupo tornar o trabalho próprio (reescrever, escutar um morador, mudar algo e entender o porquê). A IA não removeu o aviso de uso de IA. | *(preencher)* |
| 7 | 16/11/2026 | "Finge que você é um professor e avalie." | Avaliação por critério do slide 33 (nota 8,9), com pontos fracos apontados. | *(preencher)* |
| 8 | 16/11/2026 | "Então ajusta tudo isso." | Análise das definições de onda de calor (poucos eventos em 4 anos), novas variáveis de dias seguidos quentes, avaliação nos dias de onda, relatório enxuto em 2 páginas, remoção de sobras e material de estudo. | *(preencher)* |
| 9 | | | | |

## Como usamos os resultados
*(preencham: o que mudaram, quais decisões foram do grupo — por exemplo, a cidade/estação, o percentil de calor extremo, os hiperparâmetros — e o que cada um aprendeu.)*
