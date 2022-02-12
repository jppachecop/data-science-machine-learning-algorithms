# Density-Based Spatial Clustering

## Conceito:

O DBSCAN é um método de clusterização não paramétrico baseado em densidade, que é significativamente efetivo para identificar clusters de formato arbitrário e de diferentes tamanhos, identificar e separar os ruídos dos dados e detectar clusters "naturais" e seus arranjos dentro do espaço de dados, sem qualquer informação preliminar sobre os grupos. O método requer somente um parâmetro de entrada, mas dá suporte para determinar um apropriado valor para ele.

## Classes de Problemas com Melhores Resultados:

Dado que o DBSCAN é um algoritmo de clusterização baseado em densidade, ele é indicado para procurar regiões no dataset que tenham uma alta densidade de observações em contraste com aquelas que possuem uma baixa densidade de observações. Um exemplo de aplicação é recomendação de itens baseado na similaridade entre os usuários de uma plataforma.

## Definição Teórica e Modelagem Matemática:

## Vantagens:

- Excelente na separação de clusters de alta densidade dos clusters de baixa densidade dado um conjunto de dados;
- Lida bem com outliers dentro do conjunto de dados;
- Não requer a definição de um número específico prévio de clusters.

## Desvantagens (limitações):

- Tem dificuldade em lidar com clusters de densidades similares;
- Possui dificuldade em lidar com um conjunto de dados de muitas dimensões.

## Exemplo de uma Aplicação em Python:

Presente no arquivo dbscan.ipynb

## Referências:

- https://www.maxwell.vrac.puc-rio.br/24787/24787_6.PDF
- https://elutins.medium.com/dbscan-what-is-it-when-to-use-it-how-to-use-it-8bd506293818
- https://sites.google.com/site/dataclusteringalgorithms/density-based-clustering-algorithm
