# CitizenTech — alerta de calor extremo em Osasco

Global Solution 2026.2 · FIAP · Engenharia de Software (3º ano)

Integrantes: Henrique Sanches (RM557959), João Pedro Kraide Máximo (RM563166), Douglas dos Santos Melo (RM556439), Nicolas Caciolato Reis (RM556506) e Matheus Marcelino Dantas da Silva (RM556332).

## Ficha da CitizenTech

| Campo | Resposta |
|---|---|
| Nome da CitizenTech | *(o grupo define)* |
| Cidade e bairro | Osasco (SP) |
| Cidadão beneficiado | Idosos e trabalhadores de rua |
| Problema, em uma frase | Idosos e trabalhadores de rua de Osasco não recebem, com antecedência, um aviso confiável de dias de calor extremo. |
| Como funciona | Um modelo de Machine Learning (Random Forest) usa dados reais do INMET para estimar a chance de calor extremo no dia seguinte e a transforma em alerta verde, amarelo ou vermelho. *(o grupo complementa com as demais disciplinas)* |
| O que cada parte faz | **IA & Machine Learning:** pasta `ml/` (previsão e níveis de alerta). *(o grupo preenche as outras disciplinas)* |
| Link do repositório | *(o grupo cola aqui)* |
| Indicador de impacto | No teste, o modelo avisou 73% dos dias de calor extremo com 1 dia de antecedência. Nos alertas vermelhos, 68% dos dias foram realmente extremos; nos verdes, 2%. |
| ODS conectados | 3 (Saúde e bem-estar), 11 (Cidades e comunidades sustentáveis) e 13 (Ação contra a mudança global do clima) |

## Conteúdo
- `ml/`: notebook executado, dados do INMET, figuras e resultados (Inteligência Artificial & Machine Learning).
- `RELATORIO_ML.md`: relatório da disciplina de IA.
- `prompts.md`: registro do uso de IA.
