# Density-Based Spatial Clustering

## Conceito:

O DBSCAN é um método de clusterização não paramétrico baseado em densidade, que é significativamente efetivo para identificar clusters de formato arbitrário e de diferentes tamanhos, identificar e separar os ruídos dos dados e detectar clusters "naturais" e seus arranjos dentro do espaço de dados, sem qualquer informação preliminar sobre os grupos. O método requer somente um parâmetro de entrada, mas dá suporte para determinar um apropriado valor para ele.

## Classes de Problemas com Melhores Resultados:

Dado que o DBSCAN é um algoritmo de clusterização baseado em densidade, ele é indicado para procurar regiões no dataset que tenham uma alta densidade de observações em contraste com aquelas que possuem uma baixa densidade de observações. Um exemplo de aplicação é recomendação de itens baseado na similaridade entre os usuários de uma plataforma.

## Definição Teórica e Modelagem Matemática:

A ideia chave do método DBSCAN é que, para cada ponto de um cluster, a vizinhança para um dado raio contém, no mínimo, certo número de pontos, ou seja, a densidade na vizinhança tem que exceder um limiar.

Há dois parâmetros chave no DBSCAN:

- eps: a distância que especifica os vizinhos. Dois pontos são vizinhos se a distância entre eles são menor ou igual a eps.
- minPts: número mínimo de pontos para definir um cluster.

Baseado nesses dois parâmetros, os pontos são classificados como ponto central, ponto de borda ou outlier:

- Ponto central: Um ponto é um ponto central se há ao menos um número minPts aos redores dele com um raio eps;

- Ponto de borda: Um ponto é um ponto de borda se ele é alcançável por um ponto central e que haja um número minPts ao seu redor;

- Outlier: Um ponto é um outlier se não for um ponto central e não puder ser alcançado por ponto central algum.

O algoritmo do DBSCAN funciona da seguinte forma:

- minPts e eps estão determinados

- Um ponto inicial é selecionado aleatoriamente e a área de sua vizinhança é determinada utilizando um raio de valor eps. Se há ao menos um número minPts de pontos na vizinhança, o ponto é marcado como um ponto central e a formação do cluster se inicia. Se não, o ponto é categorizado como discrepante. Uma vez que a formação do cluster se inicia, todos os pontos dentro da vizinhança do ponto inicial se torna parte do cluster. Se esses novos pontos são também pontos centrais, os pontos que estão em suas vizinhanças também são adicionados no cluster.

- O próximo passo é aleatoriamente escolher os outros pontos que não passaram pelos passos anteriores.

- O algoritmo é finalizado quando todos os pontos forem testados

Aplicando esses passos, o DBSCAN pode encontrar regiões de alta densidade e separá-las de regiões de baixa densidade.

Um cluster inclui pontos centrais que são vizinhos e pontos de borda desses pontos centrais. A condição necessária para formar um cluster é ter ao menos um ponto central. Porém, pode ocorrer de existir um cluster com apenas um ponto central e seus pontos de borda.

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
- https://towardsdatascience.com/dbscan-clustering-explained-97556a2ad556
