
# Previsão de Custos Médicos

Este projeto analisa diferentes modelos de regressão para prever custos médicos, considerando variáveis como idade, IMC, filhos, gênero, status de fumante e região.

## Objetivo
Avaliar a capacidade de modelos de regressão em prever custos médicos, selecionando o modelo mais preciso com base nas métricas de avaliação.

## Metodologia e Modelos Utilizados
Modelos testados:
- **Regressão Linear**
- **Decision Tree**
- **Random Forest**
- **K-Nearest Neighbors (KNN)**
- **Support Vector Regressor (SVR)**

## Resultados e Análise
- **Melhor Modelo**: Regressão Linear com R² = 0.921 e MAE = 1595.19
- **Insights de Correlação**:
  - O status de fumante possui alta correlação com os encargos médicos (0.710), seguido por IMC e idade.
  - Abaixo, a matriz de correlação completa:

| Variável          | Idade | IMC  | Filhos | Encargos | Gênero (Masc.) | Fumante (Sim) | Região (Norte) | Região (Sudoeste) | Região (Sul) |
|-------------------|-------|------|--------|----------|----------------|---------------|----------------|-------------------|--------------|
| **Idade**         | 1.000 | 0.003| -0.006 | 0.376    | 0.001          | -0.001        | -0.008         | 0.007            | 0.001        |
| **IMC**           | 0.003 | 1.000| -0.004 | 0.447    | -0.005         | 0.018         | 0.002          | 0.004            | -0.004       |
| **Filhos**        | -0.007| -0.004| 1.000 | 0.299    | 0.004          | 0.008         | -0.010         | 0.007            | -0.005       |
| **Encargos**      | 0.376 | 0.447| 0.299  | 1.000    | -0.000         | 0.710         | -0.011         | 0.003            | 0.003        |
| **Gênero (Masc.)**| 0.001 | -0.005| 0.004 | -0.000   | 1.000          | 0.003         | 0.000          | 0.001            | 0.003        |
| **Fumante (Sim)** | -0.001| 0.018| 0.008  | 0.710    | 0.003          | 1.000         | -0.005         | -0.008           | 0.009        |

## Conclusão
O modelo de **Regressão Linear** foi o mais eficaz para prever custos médicos, capturando 92,1% da variabilidade nos dados, o que sugere uma forte linearidade entre as variáveis. A análise sugere que o status de fumante e o IMC são fatores influentes no aumento dos custos médicos.
