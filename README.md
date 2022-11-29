# MovieIt
Sistemas de Recomendação - Professor Wladmir Cardoso Brandão - PPGINF - PUCMinas

Introdução: O Problema de Recomendação:
Alvin Tofler, em 1965, em um artigo publicado na revista Horizon, apresentou o termo “future sock” onde descreve a “tensão arrasadora e a desorientação que causamos aos indivíduos ao submetê-los a excessiva mudança num espaço de tempo demasiado curto”.
Em virtude de um cenário atual onde os avanços tecnológicos presentes em todas as áreas do conhecimento humano provocam mudanças exponenciais, tornando o tempo menor do que o necessário para assimilar estas mudanças no nosso nosso dia a dia, antecipar ou tentar prever o que poe ocorrer no futuro é essencial para a nossa sobrevivência.
Desta forma, em regra geral, tem-se que os sistemas de recomendação seguem um processo bem definido a fim de criar sugestões com alto teor de precisão para nos ajudar na tomada de decisões, tendo como base fatos ou acontecimentos ocorridos no passado.
Sistemas de recomendação bem modelos podem servir tanto para tomadas de decisão positiva ou negativas, ou seja, apresentar alternativas boas ou alternativas ruins. 
Por fim, projetar sistemas de recomendação não é uma atividade trivial pois, envolve diversas áreas de conhecimento, aplicação de diversos algoritmos, fórmulas e funções para a obtenção de resultados satisfatórios, cujas variações dependem da área ou nível de precisão demandado para a solução do problema, a citar problemas da área de medicina, investimentos financerios, people analytics, dentre outros.

Sistemas de Recomendação - Base conceitual:
Em um mundo com tantas opções, os sistemas de recomendação são formados por um conjunto de algoritmos e de técnicas computacionais que possibilitam a entrega de recomendações e de sugestões de serviços ou produtos para usuários facilitando o processo de escolha.
Empresas como Amazon, Netflix e Google utilizam a recomendeação para sugerir seus produtos e serviços, melhorando a experiência de acesso do usuário e, por consequência, a receita e o valor de mercado destas organizações.
Em síntese um sistema de recomendação analisa a experiência anterior de usuários em relação à aquisição ou acesso a um item, e prevê qual seria a proposição para acessos ainda não conhecidos.
	Filtragem Colaborativa
Os sistemas de recomendação - Recommender Systems - são uma subclasse dos sistemas de filtragem colaborativa.
Filtragem colaborativa é o método que utiliza informação ou padrões anteriormente existentes, a partir de técnicas que envolvem colaboração de múltiplos agentes, pontos de vista, fontes de dados, etc.
Filtros colaborativos funcionam construindo uma base de dados de preferências de itens para usuários onde um novo usuário é comparado aos outros susuários da base de dados de forma a descobrir, utilizando algoritmos de similaridade, quais usuários mais se assemelham ao novo usuário. A partir da similaridade calculada, os itens de interesse para esses usuários da base são recomendados para o novo usuário.
Nesta abordagem o objetivo é sugerir itens que sejam similares aos que o usuário já tenha avaliado em algum momento antes:

 

Formalmente o problema de recomendação abrange três itens mínimos:
	Usuários
	Agente da ação
	Itens
	Objeto a ser consumido ou não pelo usuário
	Utilidade (nota)
	Nível de aceitação ou rejeição do objeto pelo usuário:
	Numérico – gera um problema de regrassão
	Categórico – gera um problema de classificação
Esta combinação resulta em uma relação formalmente definida:
Seja C um conjunto de usuários;
Seja S um conjunto de itens possíveis para a recomendação;
Seja u uma função de utilidade entre um usuário e um item
Temos que:
u = C x S  R
ex:
 
Onde R é um par ordenado dado por:
0 = User1 x Item1, ou seja, a relação do User2 (ci) com o item1 (si) é igual a 0 
	Medidas de similaridade
Uma vez que a filtragem colaborativa é o método que utiliza informação ou padrões anteriormente existentes, a partir de técnicas que envolvem colaboração de múltiplos agentes, pontos de vista, fontes de dados, etc. é necessário definir quais são os critérios para definir esta semelhança. Para tanto existem uma série de cálulos e comparações disponíveis para este cálculo, sendo que heurísticas podem ser permitidas, dependendo o problema, desde que devidamente fundamentadas.
A similaridade (ou a dissimilaridade) mede quanto duas instâncias são parecidas, geralmente este valor pertence a uma escala de 0 a 1 e, quanto maior o valor mais parecidas são estas instâncias. Para os casos onde os valores de u são numéricos temos um problema de regressão e o valor calculado é de dissimilaridade, e para os casos onde valores de u são categóricos o valor calculado é de similaridade.
Para instâncias numéricas a maneira mais comum para medir a similaridade entre as instâncias é o cálulo de distância. Citamos como exemplo a distância Euclidiana, o coeficiente de correlação de Pearson, a distância de Manhatan e o coeficiente de correlação Spearman como importantes medidas de similaridade. Estas medidas são definidas de acordo com o problema, esparsidade dos dados dentre outros fatores.
	Distância Euclidiana:
uma das mais populares medidas de similaridade usada, a distância Euclidiana mede a distância entre dois pontos, através da aplicação repetida do teorema de Pitágoras. Aplicando essa fórmula como distância, o espaço euclidiano torna-se um espaço métrico, com a seguinte notação:
 



d= √(∑_(k=1)^n▒〖(Pik-Pjk)〗^2 )



	Coeficiente de correlação e Pearson:
Também outra medida muito popular, o coeficiente de correlação de Pearson também chamado de "coeficiente de correlação produto-momento" mede o grau da correlação (e a direcção dessa correlação - se positiva ou negativa) entre duas variáveis de escala métrica, com a seguinte notação:
 

Diretrizes para o desenvolvimento do estudo:
O objetivo deste trabalho é propor, utilizando tarefas de filtragem colaborativa e de SVD, sistemas de recomendação de filmes do tipo user based e item based com as seguintes premissas:
	Utilizar base de dados do Projeto Movielens;
	Desenvolver as seguintes soluções:
	User Based;
	Item Based, entregando recomendações para um usuário específico
	SVD (Singular Value Decomposition)
	Apresentar o embasamento da escolha dos algoritmos algoritmos e das funções;
	Realização de Testes estatísticos para verificação de resultados. Utilizar o RMSE, podendo ser apresentadas outros testes complementares.

Sistema de Recomendação User Based
Estrutura lógica do sistema de recomendação
 
 


