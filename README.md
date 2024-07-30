# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

## 📋 Descrição

Este projeto teve como objetivo desenvolver um modelo de previsão de estoque utilizando o Amazon SageMaker Canvas. Através deste modelo, busquei prever a quantidade de estoque necessária para atender à demanda, utilizando um dataset com 1000 entradas de dados.

## 💻 Tecnologias Utilizadas

- Amazon SageMaker Canvas: Plataforma utilizada para criar e treinar o modelo de Machine Learning sem a necessidade de codificação.

- AWS: Infraestrutura de nuvem utilizada para hospedar e executar o SageMaker Canvas.

- Dataset: Conjunto de dados com 1000 entradas, contendo informações relevantes para a previsão de estoque.

## 🚀 Passos para a Realização do Projeto

## Importação do Dataset:

O dataset foi importado para o SageMaker Canvas a partir de um arquivo CSV.

## Preparação dos Dados:

Realizei a verificação e preparação dos dados, garantindo que todas as entradas estivessem completas e formatadas corretamente.

## 🎯 Seleção da Variável Alvo:

A variável alvo selecionada para o treinamento do modelo foi a quantidade de estoque.

## ✨Treinamento do Modelo:

Utilizei o SageMaker Canvas para treinar o modelo de Machine Learning, aproveitando os modelos de base prontos para uso e a interface intuitiva da plataforma.

## 👌 Avaliação do Modelo:

Após o treinamento, os resultados de desempenho do modelo foram:

- wQL(Perda moderada de quantil): 0.060 (avalia a previsão como um todo, calculando a média da precisão em pontos de distribuição específicos chamados quantis para os quantis P10, P50 e P90. Um valor mais baixo indica um modelo mais preciso);

- MAPE (Erro de percentual absoluto médio): 0.148 (é o erro percentual (diferença percentual entre o valor médio previsto e o valor real) em média em todos os pontos de tempo. Um valor mais baixo indica um modelo mais preciso com MAPE=0 como um modelo perfeito sem erros);

- WAPE(Erro Percentual Absoluto Ponderado): 0.100 (mede o desvio geral dos valores previstos em relação aos valores observados e é definido pela soma do erro absoluto normalizado pela soma da meta absoluta. Um valor mais baixo indica um modelo mais preciso com WAPE=0 como um modelo perfeito sem erros);

- RMSE(Raiz do erro quadrático médio): 5.765 (é a raiz quadrada da média quadrada dos erros. Um RMSE mais baixo indica um modelo mais preciso com RMSE=0 como um modelo perfeito sem erros);

- MASE(Erro médio absoluto em escala): 0.301 (é a média do erro absoluto da previsão normalizada pelo erro absoluto médio de um método simples de previsão de linha de base. Um valor mais baixo indica um modelo mais preciso com MASE < 1 como um modelo estimado como melhor do que a linha de base e um MASE > 1 como um modelo estimado como pior do que a linha de base).
 
Como resultado sobre os conjuntos de dados que afetam as previsões de séries temporais específica, foi apresentado que a coluna relativa aos Preços afetam em 9.61% enquanto que a coluna referente a promoções não tem impacto algum (0.00%).
