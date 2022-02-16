# K-Means Clustering

## Conceito:

O K-means é um algoritmo do tipo não supervisionado, ou seja, que não trabalha com dados rotulados.

O objetivo desse algoritmo é encontrar similaridades entre os dados e agrupá-los conforme o número de cluster passado pelo argumento k.

Este utiliza um método simples e eficiente baseado no conceito de distância.

O algoritmo de forma iterativa atribui os pontos de dados ao grupo que representa a menor distância, ou seja, ao grupo de dados que seja mais similar.

## Classes de Problemas com Melhores Resultados:

Como é um algoritmo de aprendizado não supervisionado que avalia e clusteriza os dados de acordo com suas características, como por exemplo:

- lojas/centro logistico;
- clientes/produtos ou serviços semelhantes;
- clientes/características semelhantes;
- séries/gênero da série ou faixa etaria;
- usuarios de uma rede social/usuario influenciador;
- paciente/sintoma ou característica semelhante.

Por exemplo, podemos utilizar da vantagem do agrupamento no setor comercial para identificar e segmentar perfis de clientes para uma campanha de Marketing.

Ou ainda, oferecer de forma mais assertiva um conteúdo que seja mais relevante aos clientes.

Agrupar pacientes com sintomas similares pode ser útil para identificar situações de risco em novos casos.

Segmentar produtos semelhantes pode ser extremamente interessante para um sistema de recomendação de produtos em um e-commerce.

Perceba que é bastante intuitivo que produtos similares permaneçam juntos para facilitar a navegação do usuário e incentivar a compra.

## Definição Teórica e Modelagem Matemática:

O algoritmo K-Means é um algoritmo iterativo, que particiona o dataset em K clusters pré-definidos, nos quais cada ponto deste dataset pertence a um único grupo. Ele tenta fazer os pontos dentro do mesmo cluster serem semelhantes, enquanto mantém os clusters o mais distantes possíveis. O algoritmo coloca certo pontos em um cluster dado que a soma do quadrado da distância entre os pontos e o centróide do cluster é o mínimo. Quanto menor a variação nos clusters, maior a similaridade entre os pontos dentro do mesmo cluster.

O algoritmo K-Means funciona da seguinte forma:

- Especifica o número de clusters K
- Inicializa centróides ao selecionar randomicamente K pontos para os centróides sem substituição
- Continua iterando até não haver mais mudanças nos centróides, ou seja, a atribuição de pontos para os clusters não estar mudando.

## Vantagens:

- Simples para implementar
- Escalável
- Garante convergência
- Adaptável a novos exemplos
- Generelizável a cluster de diferentes formas e tamanhos

## Desvantagens (limitações):

- Necessidade de escolher k manualmente
- Dependente de valores iniciais
- Clustering dados de tamanhos e densidades variáveis
- Não é escalável com o aumento do número de densidades

## Exemplo de uma Aplicação em Python:

Presente no arquivo kMeansClustering.ipynb

## Referências:

- https://minerandodados.com.br/entenda-o-algoritmo-k-means/#tipos_cluster_grupos
- https://medium.com/programadores-ajudando-programadores/k-means-o-que-%C3%A9-como-funciona-aplica%C3%A7%C3%B5es-e-exemplo-em-python-6021df6e2572
- https://towardsdatascience.com/k-means-clustering-algorithm-applications-evaluation-methods-and-drawbacks-aa03e644b48a
- https://developers.google.com/machine-learning/clustering/algorithm/advantages-disadvantages
