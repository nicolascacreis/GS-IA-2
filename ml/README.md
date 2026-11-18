# ml/ — Inteligência Artificial & Machine Learning (GS CitizenTech)

Pergunta de ML: **amanhã será um dia de calor extremo?** (Random Forest, dados reais do INMET).

## Como rodar
1. `pip install -r requirements.txt`
2. Baixe os dados do INMET e coloque em `dados/raw/` (passo a passo em `dados/README.md`).
3. Abra `citizentech_calor_extremo.ipynb` (Jupyter, VS Code ou Colab) e execute **Restart & Run All**.
   - Rode com a pasta `ml/` como diretório de trabalho. No Colab, envie a pasta `ml/` inteira.
4. O notebook gera as figuras em `figuras/` e as tabelas em `resultados/`.
5. Salvem o notebook **com as saídas** e façam o commit.

## Trocar cidade/estação
Edite a célula "CONFIGURAÇÃO" do notebook (`CIDADE`, `ESTACAO`, `ANOS`). O código encontra os arquivos pelo código da estação no nome do CSV.

## Estrutura
```
ml/
├── citizentech_calor_extremo.ipynb
├── requirements.txt
├── dados/ (README.md + raw/)
├── figuras/
└── resultados/
```

O relatório (`RELATORIO_ML.md`) fica na raiz do repositório.
