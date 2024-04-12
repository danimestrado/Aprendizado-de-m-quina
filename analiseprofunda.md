**Análise sobre o capítulo 0 do livro o "The Principles of Deep Learning Theory" **

Para o estudo da deep learning, o autor explica que os conceitos microscópicos e macroscópicos são apresentados seguindo a tradição da física teórica, a qual encontra teorias simples e eficazes para soluções complexas, como por exemplo, a termodinâmica e mecânica estatística, onde chega a fazer comparações com a deep learning. 

Ele explica que uma rede neural em sua essência serve como uma receita para calcular funções construídas a partir de um grande volume de unidades computacionais, que nesse caso são denominadas como neurônios.  Cada neur	ônio é uma função simples que considera uma soma ponderada de sinais recebidos disparados como características, comparando o valor dessa soma com algum limite determinado. Além disso, os neurônios são organizados em camadas paralelas, e as redes neurais profundas são compostas por múltiplas camadas em sequência. 

Os parâmetros das redes são limites de disparos e conexões ponderadas entre os neurônios. Pode-se definir uma rede neural como uma função parametrizada: f(x;), em que “x” é a entrada da função, e o "” é o parâmetro vetorial desse “x” que controla a forma da função. Para que a função funcione como esperado, é necessário ajustar esse vetor de parâmetros de alta dimensão, onde é realizado a partir de duas etapas.

A primeira etapa é inicializar a rede amostrando aleatoriamente o vetor de parâmetros "" a partir de uma distribuição de probabilidade computacionalmente simples, denominada p(). A segunda etapa é o ajuste do parâmetro vetorial  para *, de modo que a função resultante da rede seja:  f(x;*), se aproximando o máximo possível da função desejada f(x).

Esse processo é conhecido como aproximação da função. Para encontrar os ajustes no parâmetro vetorial *, é necessário realizar ajustes na função de rede inicial, f(x;), com os dados de treinamento, formando variáveis pares “ x,f(x)”, observador a partir do desejado, ou seja, a função alvo. 

Esses ajustes nos parâmetros é chamado de treinamento, e o procedimento específico utilizado para ajustá-los é chamado de algoritmo de aprendizagem. Para visualizar mais diretamente os tipos de problemas técnicos futuros, o livro aborda sobre a expansão de Taylor, em que a função "f(x;*)”, é expandida e mostrando três tipos de problemas principais. 

O primeiro problema é que essa expansão de Taylor pode conter infinitos números de termos, e a medida que aumenta a distância entre os parâmetros , *, aumenta o número desses termos. 

O segundo problema é que a cada inicialização de parâmetros, teremos diferentes funções de redes, visto que os parâmetros são aleatoriamente amostrados da distribuição p(). Assim, a inicialização induz uma distribuição sobre a função de rede e suas derivadas, e para isso é necessário determinar um mapeamento, levando uma distribuição dos parâmetros iniciais à distribuição conjunta da função de rede, f(x;), seu gradiente, dfd, e a sua Hessiana,d2fd2 e assim por diante. 

No terceiro problema é mostrado que o valor aprendido dos parâmetros, *, é o resultado de um processo complicado de treinamento e em geral, esse valor não é único e pode ser dependente de muitas outras variáveis. Na prática, esse valor é iterativo e vai acumulando as mudanças a cada etapa e a dinâmica é não-linear. 

Como resolução desses problemas citados acima, o autor aborda outros princípios, como por exemplo o princípio da dispersão. Nesse princípio devemos ter alguns conhecimentos prévios. As duas partes essenciais da arquitetura de uma rede neural são a largura (n), e a profundidade (L) e para fazer simplificações em sua quantidade de componentes, deve-se ter em mente que os componentes de uma rede são os neurônios e eles podem ser aumentados ou minimizados a partir de mudanças nos valores da largura ou profundidade, e saber que existem diversas simplificações no limite de um grande número de componentes.

Para realizar essa simplificação, o autor delimita a função do limite,  sendo: lim n p(f*), sendo necessário o estudo de uma rede neural idealizada nesse limite. Isso é conhecido como “limite de largura infinita”, e se esse limite estiver no extremo, isso simplificará a distribuição das redes treinadas, p() , resolvendo os três primeiros problemas. 

Para o primeiro problema, se desconsiderarmos todas as derivadas acima da ordem 2 e da ordem 2, podemos manter apenas dois termos, diminuindo o problema de infinitos termos. Para o segundo problema, as distribuições das funções aleatórias serão independentes para cada termo de distribuição marginal em uma forma simples.

Para o terceiro problema, o treinamento se torna linear e independente das variáveis do algoritmo de aprendizagem, possibilitando encontrar uma função analítica de forma fechada para o parâmetro *.

Como resultado, a distribuição treinada é uma simples distribuição Gaussiana com uma média diferente de zero, e assim podemos visualizar de forma simples as funções da que a rede está computando.  Essas simplificações são consequências do princípio da dispersão, pois mesmo que pareça que a rede esteja ficando mais complicada ao aumentar a sua largura tendendo ao infinito, as complexidades da rede se tornam mais gerenciáveis. Apesar disso, pode haver eliminação de pequenos detalhes de cada neurônio e também o princípio assume uma idealização que pode não ser prática ou realizável, demonstrando a quebra da correspondência entre a teoria e a realidade.

A teoria da perturbação, ao invés de considerar larguras infinitas, propõe utilizar uma expansão 1/n, sendo n a largura da camada, para incluir correções e obter uma descrição mais precisa da rede. Para a solução dos três problemas iniciais, temos para o primeiro problema, o tratamento de derivadas de alta ordem da função de rede, onde termos com derivadas de ordem maior que três contribuem com pouco para o comportamento da rede e podem ser ignorados.

Para o problema 2, a inicialização aleatória dos parâmetros da rede implica que a distribuição de funções da rede é também aleatória. No entanto, no limite de largura grande, essa distribuição é quase simples, e pode ser tratada com teoria da perturbação.

E, por fim, para o terceiro problema utiliza-se uma teoria da perturbação dinâmica para lidar com o processo não-linear de treinamento, permitindo uma solução analítica para os parâmetros otimizados da rede.

Isso mostra que, usando a expansão em 1/n, pode-se desenvolver uma teoria efetiva para entender as redes neurais. Essa abordagem é mais prática e realista do que usar uma aproximação de largura infinita e permite análises matemáticas das propriedades da rede.

A distribuição dos parâmetros treinados da rede, quando considerada no nível de correção 1/n, tende a uma distribuição quase-Gaussiana. Isso implica que as propriedades estatísticas da rede treinada podem ser aproximadas por uma distribuição normal, o que simplifica significativamente a análise teórica.

A distribuição treinada reflete a interação entre os neurônios e depende de maneira não trivial do algoritmo de aprendizagem utilizado, assim como do processo de representação na rede. Isso torna a descrição teórica mais alinhada com o que é observado em redes neurais reais, tornando-a um modelo teórico minimamente complexo, mas ainda assim útil para entender o aprendizado profundo.

Ao expandir em séries, termos de ordem superior na expansão podem ser necessários para uma descrição mais fina. Embora o cálculo desses termos seja sistematicamente possível, o texto indica que a compreensão do erro de truncamento fornece uma noção mais profunda de quando a série pode ser truncada com segurança sem perder informações significativas.

A relação profundidade e largura (r=L/n), podemos concluir que Em redes de largura infinita, as interações entre os neurônios são praticamente nulas, tornando essa descrição suficiente. No entanto, estas redes são essencialmente superficiais, pois não possuem profundidade relativa.

Em redes finitas, ocorrem interações não triviais entre os neurônios, e as correções de ordem 1/n se tornam importantes. Estas redes são consideradas efetivamente profundas, e o “r” fica entre 0 e 1.

Quando o “r” é maior que 1, temos que os neurônios estão fortemente acoplados, o que pode levar a comportamentos caóticos, e uma descrição efetiva se torna inviável devido a grandes flutuações.

A maioria das redes neurais usadas na prática possui uma relação profundidade-largura que permite que a expansão truncada em 1/n seja uma descrição precisa. Isto implica que para muitas redes reais, as interações complexas podem ser aproximadas de forma efetiva usando apenas os termos de primeira ordem da expansão.

A partir disso, pode-se concluir que para descrever adequadamente as propriedades de redes neurais multicamadas, ou seja, para compreender o aprendizado profundo, é necessário estudar redes de largura grande, porém finita. Desta forma, seremos capazes de encontrar uma descrição teórica eficaz em larga escala de redes neurais profundas realistas.


