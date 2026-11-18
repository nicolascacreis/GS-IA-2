# Dados — INMET (estação automática A701, São Paulo – Mirante de Santana)

Dados **reais e públicos**. Nenhum dado simulado é usado neste projeto.

| Item | Descrição |
|---|---|
| **Fonte** | INMET (Instituto Nacional de Meteorologia), Banco de Dados Meteorológicos, dados históricos horários |
| **Link** | https://portal.inmet.gov.br/dadoshistoricos |
| **Estação** | A701, São Paulo – Mirante (Mirante de Santana, SP). É a estação automática do INMET mais próxima de **Osasco**, a cerca de 18 km (distância informada pelo portal do INMET na página de previsão da cidade) |
| **Período usado** | 01/01/2022 a 31/12/2025 (4 anos; ajustável em `ANOS`, na célula de configuração do notebook) |
| **Granularidade original** | 1 registro por hora; o notebook agrega para 1 linha por dia (horário de Brasília) |
| **Data de acesso** | 16/11/2026 *(corrijam se o download foi em outro dia)* |

## Como baixar
1. Abra o link acima e baixe o `.zip` de cada ano (2022 a 2025).
2. Dentro de cada zip há um CSV por estação. Extraia o arquivo cujo nome contém **A701** (ex.: `INMET_SE_SP_A701_SAO PAULO - MIRANTE_01-01-2023_A_31-12-2023.CSV`) para `ml/dados/raw/`.
3. Se o notebook não achar algum ano, ele tenta baixar sozinho; se o portal bloquear, siga os passos acima.

Os 4 CSV brutos da A701 (2022 a 2025) já estão em `ml/dados/raw/` e não devem ser editados à mão.

## Colunas usadas (nomes originais do INMET)
Temperatura do ar (bulbo seco), temperatura máxima e mínima na hora anterior, umidade relativa, precipitação total, radiação global, velocidade do vento e pressão atmosférica ao nível da estação.

## Tratamentos aplicados no notebook
- 8 linhas de metadados ignoradas; separador `;` e decimal `,`.
- Valor `-9999` = dado ausente.
- Horas em UTC convertidas para UTC−3 (simplificação: não trata o horário de verão de anos antigos).
- Dias com menos de 18 horas válidas são descartados; lacunas de até 2 dias são interpoladas.
- A cobertura de dias válidos por ano é impressa no notebook.

## Cuidados
Os dados são de uma única estação, fora de Osasco (~18 km), e não representam diferenças de temperatura entre bairros. Isso é uma limitação declarada no relatório.
