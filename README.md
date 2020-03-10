# classificador_projeto_2
Projeto #2 - Classificador Supervisionado


Anotacoes da aula #23 para aplicar no projeto 2: 

Aula #23
objetivo de se utilizar os algoritmos de ML.
R: mostrar o comportamento dos dados. 

perceptron eh o algoritmo mais simples de ML. 

se seu dado e 100% aleatorio nas faz sentido um algoritmo de aprendizado. Agora se seu dado tem uma padrao, e se existe em funcao, conseguiremos aplicar algoritmos de ML.

nao sao problemas que possuem uma solucao obvia. trade-off
cross validation => 
  overfit : queremos o meno erro, mas nem tanto
  underfit : queremos o modelo mais simples, mas que seja o bom o suficente. 

  dica de modo geral: nao ha regras de ouro e verdades absolutas. Estamos num ambiente mais movedico.

exemplo do desastre de Fukishima

mais dois conceitos
  vies : hipotese assumidas previamente: "meu dado por ser representado por uma reta" 
  variancia : o quanto que o dado previne o treino
alto vies e baixa variancia ==> underfit (a funcao nao esta tao associada com o dado de treino e vies alto, onde vc assume que o dado pode ser escrito pela funcao de uma reta, por exemplo)
baixo vies e alta variancia ==> overfit (dado depende muito do treino, bom resultado no treino)
o proposito e achar um modelo que equilibra. 

underfit => o modelo nao conseguiu descrever a funcao. Nao conseguiu fazer o fit da maneira necessaria

overfit ==> tem um erro no treino sensacional (baixo) e a validacao e alta (erro na validacao alto).

curva de aprendizado. comparar as curvas de teste e aprendizado eh importante.

como lidar com o problema de overfit e underfit
* underfit => aumentar a complexidade. Se trabalhou com perceptron, utilizar um algoritmo mais complexo.
* overfit => 
  cross validation eh uma ferramenta importante para verificar o overfit
  adquirir mais dado (nem sempre o melhor caminho)
  reduzir a dimensionalidade. o que e isto? reduzir feature. Conhecimento de dominio de negocio. hoje temos varias bibliotecas que ajudam a explicar o resultado de alguns algoritmos. 
  early stop
  regularizacao. regularizar o modelo pela quantidade de nos na arvore. Quando a arvore come a crescer demais, a funcao de perda diminuiu, mas se penaliza para complexidade

PRINCIPIOS PARA CONSTRUIR UMA BOA SOLUCAO
* conheca o seu problema/dominio. Faca analises exploratorias sobre seus dados
* prepare seu dado (normalize, limpe, transforme)
* defina uma metrica de sucesso
* esoclha um modelo 
* construa um baseline
* acompanhe os resultados em producao
* realize ciclos de melhorias (hiperparametros, melhoria do modelo, dados).

a melhor forma de combater vies eh ter um time multidisciplinar!!!
