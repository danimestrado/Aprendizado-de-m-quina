**Resumo sobre o capítulo 4 do livro**

Os dados de treinamento apesar de muitos não darem a devida importância é essencial para acrescentar melhorias e aumentar o desempenho dos modelos de aprendizado de máquina. Muitos dados coletados podem vir complexos, imprevisíveis, muito aleatórios ou até mesmo confusos, se eles não forem tratados corretamente, podem prejudicar a operação do aprendizado de máquina, para isso o capítulo abordou diferentes técnicas para criar bons dados de treinamento na fase de desenvolvimento de um aprendizado de máquina. 

**10 Insights conceituais**

1. Amostragem não-probabilística é quando a seleção de dados não é baseada em nenhum critério de probabilidade. Os critérios considerados para esse tipo de amostragem são: o critério de  amostragem de conveniência, em que os dados são selecionados com base na sua disponibilidade; o critério de bola de neve, que tem como base a seleção de amostras futuras em relação a amostras existentes; o critério de julgamento, onde os desenvolvedores decidem quais amostrar irão incluir; e por fim,  o critério de cota, onde as amostras são selecionadas em cotas para determinadas partes de dados sem aleatoriedade.

2. A amostragem aleatória simples ocorre quando todas as amostras de um total têm probabilidades iguais de serem selecionadas, é de fácil implementação, porém os dados de interesse podem não aparecer na seleção.
  
3. A amostragem estratificada é uma melhoria da anterior, pois a seleção ocorre após a divisão da população em grupos de interesse, esse método nem sempre é possível, pois uma amostra pode pertencer a diversos grupos.
     
4. A amostragem ponderada ocorre quando a amostra tem consigo um peso que determina a probabilidade dela ser selecionada.

5. A amostragem de reservatórios é quando as amostras estão reservadas em matrizes, e possuem chances iguais de serem selecionada

6. A amostragem de importância permite fazer amostragens de uma distribuição quando se tem acesso previamente de outra distribuição.

7. A maioria dos modelos de aprendizado de máquina em produção atualmente são supervisionados, esse modelo necessita de dados rotulados para aprender. Existem diversos desafios para rotular os dados de interesse, são eles: rotulagem manual, esse tipo de rotulagem diminui a rapidez de iteração e torna o modelo menos adaptável a ambientes e requisitos variáveis; múltiplos rótulos, quando os dados possuem diferentes fontes é comum que possuam diferentes níveis de precisão, podendo levar ao problema de ambiguidade ou multiplicidade dos rótulos; linhagem de dados, ao utilizar dados de diferentes fontes, gerados com diferentes anotadores, o desempenho do modelo diminui, pois não se é examinado sua qualidade precedente.

8. Os rótulos naturais tornam as previsões dos modelos capazes de serem avaliadas automaticamente ou parcialmente pelo sistema.

9. Lidando com a falta de rótulos: quando não se há aquisição de rótulos suficientes de alta qualidade, algumas técnicas foram desenvolvidas para sanar esse problemas. São elas: a supervisão fraca, semi-supervisão, aprendizagem por transferência e aprendizagem ativa.

    Todas elas se aproveitam de alguma alternativa que gera mais rótulos. A supervisão fraca aproveita as heurísticas, a semi-supervisão aproveita suposições estruturais, a transferência de aprendizagem aproveita de modelos pré-treinados e o aprendizado ativo aproveita de dados que sejam mais úteis para o seu modelo

10. A técnica de aumento de dados é usada em casos em que se tem dados de treinamento limitados, como por exemplo, imagens médicas, o aumento de dados faz com que os modelos se tornem mais robustos a ruídos e se tornou etapa padrão em visão computacional.  Existem 3 tipos principais de aumento de dados, a transformação simples de preservação de rótulos, perturbação e síntese de dados.

A transformação simples de preservação de rótulos é uma técnica simples que modifica aleatoriamente uma imagem preservando seu rótulo, seja cortando, invertendo, girando ou até mesmo apagando uma parte da imagem. Essas mudanças não alteram o significado original da imagem, e por isso esse tipo de aumento de dados é uma maneira rápida de duplicar ou triplicar os dados de treinamento. 

A técnica de perturbação também preserva os rótulos, ela adiciona uma pequena quantiade de ruído a uma imagem, podendo fazer com que uma rede neural classifique-a incorretamente. Essa é uma técnica para criar amostras diversificadas, podendo ajudar os modelos a reconhecer os pontos fracos em seus limites de decisão aprendidas e melhorar seu desempenho. Por fim, a técnica de síntese de dados é utilizada para aumentar o desempenho de um modelo, pois a coleta de dados é um processo caro e lento.

**Conclusão**

Pode-se observar que os dados podem vir de diferentes fontes, tornando-os confusos, trazendo às vezes dados fora do interesse da amostra, e para isso as técnicas citadas acima ajudam a melhorar a qualidade dos dados, visto que a qualidade e quantidade são essenciais para um melhor modelo de aprendizado de máquina. Foi mostrado também técnicas que ensinam a acrescentar dados quando se tem poucas amostras, bem como, rotular os dados em caso de falta de rótulos neles.
