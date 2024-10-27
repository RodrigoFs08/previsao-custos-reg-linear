
# Previsão de Custos Médicos

Este projeto analisa diferentes modelos de regressão para prever custos médicos, considerando variáveis como idade, IMC, filhos, gênero, status de fumante e região.

## Objetivo
Avaliar a capacidade de diferentes modelos de regressão para prever custos médicos com base em variáveis como idade, IMC, número de filhos, gênero, status de fumante e região.

## 1. Metodologia e Modelos Utilizados
Nesta análise, foram testados cinco modelos de regressão:

- **Regressão Linear**: Utilizado para verificar uma relação linear entre as variáveis.
- **Decision Tree**: Modelo não linear que divide o espaço dos dados em regiões, permitindo capturar relações complexas.
- **Random Forest**: Conjunto de múltiplas árvores de decisão, mais robusto a variáveis ruidosas.
- **K-Nearest Neighbors (KNN)**: Baseado na proximidade entre os pontos, útil para captar padrões locais.
- **Support Vector Regressor (SVR)**: Modelo que busca maximizar a margem entre pontos, porém apresentou menor desempenho nesta análise.

## 2. Correlação entre Variáveis
A tabela a seguir apresenta a matriz de correlação entre as variáveis:



### Observações da Correlação
- O status de fumante apresentou uma correlação alta e positiva com os encargos (0.710), indicando que fumar tende a aumentar os custos médicos.
- O IMC e a idade também mostraram correlações moderadas com os encargos (0.447 e 0.376, respectivamente), sugerindo uma relação entre maior IMC/idade e custos médicos mais elevados.

## 3. Resultados dos Modelos Testados
As métricas de avaliação dos modelos (R²) foram as seguintes:

- **Regressão Linear**: 0.9222
- **Decision Tree**: 0.8322
- **Random Forest**: 0.9066
- **K-Nearest Neighbors**: 0.9025
- **Support Vector Regressor**: 0.1219

A **Regressão Linear** apresentou o melhor desempenho com um R² de 0.921, indicando que explica aproximadamente 92,1% da variabilidade dos custos médicos.

## 4. Análise de Erro e Precisão do Melhor Modelo
Para o modelo de **Regressão Linear**, foram calculadas as seguintes métricas adicionais:

- **MAE (Erro Médio Absoluto)**: 1595.19
- **R² (Coeficiente de Determinação)**: 0.921

Abaixo, o gráfico de dispersão entre as previsões do modelo de Regressão Linear e os valores reais dos encargos médicos. A linha de identidade mostra onde as previsões coincidem com os valores reais, evidenciando a precisão do modelo.

** graficos aqui**

## 5. Conclusões
- O modelo de **Regressão Linear** foi o mais eficaz para prever custos médicos, capturando 92,1% da variabilidade nos dados, o que sugere uma forte linearidade entre as variáveis.
- A correlação alta do status de fumante e IMC com os encargos reforça a importância dessas variáveis nos custos médicos.
