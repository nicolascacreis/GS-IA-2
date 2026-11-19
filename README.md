# SombraViva — Inteligência Climática Urbana

Parte de **Inteligência Artificial & Machine Learning**: alerta de calor extremo em Osasco.

Global Solution 2026.2 · FIAP · Engenharia de Software (3º ano)

Integrantes: Henrique Sanches (RM557959), João Pedro Kraide Máximo (RM563166), Douglas dos Santos Melo (RM556439), Nicolas Caciolato Reis (RM556506) e Matheus Marcelino Dantas da Silva (RM556332).

Vídeo da disciplina de IA: https://youtu.be/NS8OXKUnSUg

## Ficha da CitizenTech

| Campo solicitado | Resposta da equipe |
|---|---|
| Nome da CitizenTech | **SombraViva — Inteligência Climática Urbana** |
| Cidade e bairro | **Osasco (SP), região central.** Estudo inicial no Calçadão da Rua Antônio Agú; os locais exatos dos futuros sensores ainda dependem de estudo de campo. |
| Cidadão beneficiado | Pedestres, trabalhadores expostos ao sol, pessoas idosas, comerciantes e gestores de planejamento urbano. |
| Problema, em uma frase | A população e os gestores têm dificuldade de acessar informações contextualizadas e verificáveis sobre exposição ao calor, presença de sombra e vegetação nos espaços públicos. |
| Como funciona | Uma API REST integra leituras de sensores, banco de dados e fontes meteorológicas externas; um observatório web apresenta séries, comparações e seus limites de proveniência; um painel administrativo registra e investiga eventos de segurança. |
| O que cada parte faz | **SOA:** FastAPI, endpoints REST, autenticação, MySQL, Swagger e migrações. **IoT:** ESP32 e DHT22 (Wokwi) e envio de leituras autenticadas, inicialmente simuladas. **Cybersecurity:** proteção de PII, JWT, auditoria, alertas e triagem. **Web:** visualização de temperaturas e contexto urbano, diferenciando estimativas, dados reais e simulações. **IA & Machine Learning (este repositório):** modelo Random Forest, treinado com dados reais do INMET, que estima a chance de calor extremo no dia seguinte e a transforma em alerta verde, amarelo ou vermelho (pasta `ml/`). |
| Link do repositório | **IA & Machine Learning:** https://github.com/nicolascacreis/GS-IA-2 · **SOA e Cybersecurity:** https://github.com/JoaoKraideM/sprintSoaCyber |
| Indicador de impacto | **Indicador proposto:** quantidade de locais com leituras válidas e cobertura temporal do monitoramento, comparável por período, com base nisso levantamento de dados em tempo real, unificando um desenvolvimento sustentável junto de um futuro verde. Indicadores secundários: estações ativas e utilização do portal. |
| Indicador da parte de IA | No teste, o modelo avisou 73% dos dias de calor extremo com 1 dia de antecedência. Nos alertas vermelhos, 68% dos dias foram realmente extremos; nos verdes, 2%. |
| ODS conectados | **ODS 3** — Saúde e Bem-Estar; **ODS 11** — Cidades e Comunidades Sustentáveis; **ODS 13** — Ação Contra a Mudança Global do Clima. |

## Parte de IA & Machine Learning

- **Pergunta:** com as medições de hoje, amanhã será um dia de calor extremo (máxima ≥ 32,5 °C)?
- **Dados:** reais e públicos, do INMET (estação A701, São Paulo – Mirante, a cerca de 18 km de Osasco), de 2022 a 2025. Nenhum dado simulado nesta parte.
- **Modelo:** Random Forest, com 18 combinações de hiperparâmetros e validação cruzada temporal só no treino.
- **Relatório:** [`RELATORIO_ML.md`](RELATORIO_ML.md)
- **Notebook executado:** [`ml/citizentech_calor_extremo.ipynb`](ml/citizentech_calor_extremo.ipynb)
- **Como rodar:** [`ml/README.md`](ml/README.md)

## Conteúdo do repositório

- `ml/`: notebook executado, dados do INMET, figuras e resultados.
- `RELATORIO_ML.md`: relatório da disciplina de IA.
- `prompts.md`: registro do uso de IA.
