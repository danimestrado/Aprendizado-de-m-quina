O capítulo inicia mostrando o caso em que você deseja identificar se aquela mensagem é spam ou não, para isso, precisamos entender que em uma mensagem podem conter “n” números de itens, como sílabas, letras, palavras, fonemas, entre outros, ou seja, um “n-grama” se refere a sequência de n itens de um simples texto. 

  Entretanto, além desses elementos deve-se ter outras informações, como o comentário, quem postou/enviou, tópico em que foi postado. Isso pode deixar o processo lento e complexo e para isso diversas operações foram criadas no âmbito de aprendizado de máquina para agilizar esse processo. 

  Um dos primeiros problemas citados foi a falta de valores em alguns dados, como por exemplo uma linha do excel com diversas colunas de variáveis, porém algumas variáveis não estão preenchidas. Na maioria dos casos, se tem como solução deletar esses dados com variáveis faltantes por ser um método fácil de se fazer. 

  Existem diversas formas de deletar esses dados, se por acaso mais de 50% variáveis estiverem sem valores, é mais fácil deletar todo o dado, se apenas uma variável não tiver preenchida com o valor, remove apenas ela, porém pode retirar importantes informações para o treinamento do modelo.

  Outra forma de resolver esse problema de valores vazios, seria preencher com a média, mediana ou moda de todos os valores daquela variável. Porém, para todas as formas de resolver esse problema, nenhuma vai ser 100% adequada, e para isso deve-se analisar o caso em particular e ver o que é mais interessante para aquele modelo. 

  A próxima operação citada é a de “feature scaling”, ou seja, escalonamento de recursos, a qual ajuda a normalizar as variáveis que estejam na mesma escala.  Isso é crucial porque modelos de ML, como árvores de decisão e regressão logística, podem interpretar erroneamente a importância dos recursos se eles estiverem em diferentes magnitudes.

Em casos que temos valores próximos, porém com representações discretas, como por exemplo 10,000 e 90,000.50, o modelo pode tratar diferentemente esses dois valores, para ensinar ao modelo de que são valores próximos e não tão distintos assim, se usa a operação de discretização, em que, transforma um recurso contínuo em um discreto recurso, ou seja, coloca-os em um intervalo de valores, denominados de categorias, tanto para valores contínuos como discretos. 

Para os desafios de codificação de características categóricas, especialmente em ambientes de produção onde as categorias podem mudar ao longo do tempo, temos que elencar alguns pontos-chaves, ao contrário da suposição comum de que as categorias são estáticas, em produção elas podem mudar, o que significa que novas categorias podem surgir e algumas existentes podem desaparecer; ao construir um modelo de recomendação para produtos da Amazon, é destacado o desafio de lidar com milhões de marcas diferentes. Atribuir a cada marca uma codificação numérica estática pode causar problemas, pois novas marcas são constantemente adicionadas.

Para resolver o problema de encontrar marcas desconhecidas durante a produção, é sugerido criar uma categoria "UNKNOWN" para marcas não vistas durante o treinamento. Isso evita que o modelo falhe ao encontrar uma marca nova. O modelo inicialmente só lida com as marcas mais populares (top 99%) e categoriza o resto como desconhecidas. Isto é feito para que o modelo pelo menos saiba lidar com entradas não vistas durante o treinamento.

  Apesar dessa solução inicial, os problemas surgem quando o modelo não consegue distinguir entre os diferentes tipos de marcas desconhecidas, tratando marcas de luxo novas e marcas falsificadas da mesma forma, por exemplo, como as características categóricas estão em constante evolução, é difícil sua categorização em grupos fixos. 

  Uma solução apresentada para esse problema é o uso do "hashing trick", que permite codificar categorias dinâmicas. O truque consiste em aplicar uma função de hash para transformar categorias em índices numéricos dentro de um espaço de hash predefinido, evitando a necessidade de conhecer todas as categorias possíveis antecipadamente.

  Ao especificar o espaço do hash, é possível controlar o número de valores codificados para uma característica, permitindo que o modelo antecipe e trate adequadamente novas categorias. Colisões (duas categorias distintas recebendo o mesmo índice de hash) podem acontecer, mas geralmente são aleatórias e, portanto, menos problemáticas do que tratar todas as novas categorias como desconhecidas. 

  O hashing permite que o modelo trate categorias desconhecidas de maneira mais robusta, evitando problemas que surgem quando novas categorias são tratadas da mesma forma que categorias impopulares conhecidas, garantindo que o modelo se adapte mais eficazmente a dados em constante mudança. O texto sugere que você pode escolher um espaço de hash suficientemente grande para reduzir a chance de colisões, que é quando diferentes categorias recebem o mesmo valor de hash.

É recomendado escolher funções de hash que atribuam valores próximos a categorias similares, como sites com nomes parecidos, para manter uma certa continuidade e proximidade entre as características. O hashing trick pode ser particularmente útil em cenários de aprendizado contínuo (continual learning), onde modelos aprendem a partir de exemplos que chegam continuamente.

 Feature crossing é usado para modelar interações complexas, por exemplo, a relação não linear entre estado civil e número de filhos, criando um novo recurso que combina ambos. Essa técnica é particularmente valiosa para modelos que não aprendem naturalmente relações não lineares, como regressão linear, regressão logística e modelos baseados em árvores. Em redes neurais, pode ser menos importante, mas ainda é útil para acelerar o aprendizado e melhorar a interpretação do modelo.
Uma de suas desvantagens é que o excesse de feature crossing  pode aumentar a complexidade do modelo e levar ao overfitting, pois o modelo pode se tornar muito específico para os dados de treinamento.
  
O vazamento de dados, “Data Leakage”, refere-se ao fenômeno quando uma forma do rótulo “vaza” no conjunto de recursos usados ​​para fazer previsões, e essa mesma informação não está disponível durante a inferência. Esse é um desafio, pois muitas vezes o vazamento não é óbvio, fazendo com que os modelos falham de forma inesperada.
Os tipos de Data Leakage são: informações futuras, usar dados de treinamento que inadvertidamente incluem informações do futuro (dados que só seriam conhecidos após o evento de interesse); separação incorreta de dados, divisão inadequada do conjunto de dados que resulta em sobreposição entre os conjuntos de treinamento e teste.
As causas comuns são: escalonamento usando dados de teste, calcular estatísticas para o escalonamento de recursos usando todo o conjunto de dados, incluindo o conjunto de teste; preenchimento de valores ausentes, imputar valores ausentes usando estatísticas de todo o conjunto de dados; duplicação de dados e vazamento de grupo.
Para a detecção e prevenção, temos o monitoramento de cada etapa do processo de modelagem, e avaliação da importância de cada recurso e investigar quaisquer correlações anormalmente altas com a variável-alvo. 
  
O autor discute a importância de criar características (features) que não apenas melhoram o desempenho do modelo, mas também generalizam bem para dados não vistos. As boas práticas em engenharia de recursos ajudam a construir modelos mais robustos e confiáveis. Por fim, aqui estão os pontos essenciais destacados:

Seleção de Recursos: A seleção de recursos adequados é essencial para desenvolver modelos eficazes. Isso envolve identificar quais recursos têm a maior influência sobre a variável de interesse e podem melhorar a precisão das previsões.

Feature Importance: Para avaliar a importância dos recursos, técnicas como a análise SHAP (SHapley Additive exPlanations) podem ser usadas para entender a contribuição de cada recurso para as previsões do modelo.


Feature Generalization: Recursos devem ser relevantes e generalizáveis aos dados que o modelo encontrará em uso real. Isso significa que eles devem ser representativos das variáveis subjacentes e não apenas dos padrões encontrados no conjunto de treinamento.

Avoiding Overfitting: Muitos recursos podem levar a um ajuste excessivo (overfitting), onde o modelo se ajusta muito bem aos dados de treinamento, mas falha ao prever novos dados. É importante equilibrar a quantidade de recursos para evitar a complexidade desnecessária.

Feature Stores: A discussão adianta que repositórios de recursos (feature stores) podem ajudar na gestão e reutilização eficiente de recursos em diferentes modelos e projetos, apontando para uma discussão mais aprofundada no Capítulo 10.

Avaliação Contínua: A engenharia de recursos é um processo iterativo que requer avaliação e ajustes contínuos à medida que novos dados são coletados e novas informações se tornam disponíveis.
 
  
