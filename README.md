Projeto - Detecção de Anomalias em Transações em Python

Esse projeto tem o foco em treinar modelos na detecção de fraúdes bancárias. Sendo um desafio bastante incomum em ser realizado por causa do desbalanceamento de dados encontrados no dataset, onde procurarmos fazer com que a máquina possa avaliar e alertar as transações que são considerada como "Fraúde" que apenas acontecem 0.17% das vezes.

Para enfrentar esse problema, foi criado dois tipos de dados chamados "Amount_log" e "Amount_scaled", tornando o valor do dado "Amount" mais maleável na realização da etapa do treinamento de máquina. Além disso, devido ao alto número de outliers entre os dados encontrados, houve-se a necessidade de tráta-los através da transformação desses valores, detectando-os usando a fórmula IQR, e transformando-os em média para que a detecção de fraude seja mais preciso em avaliar valores mais sútis.

Foi treinado e utilizado vários modelos: RandomForestClassifier, DecisionTree, Naive Bayes e finalmente XGBoost. Sendo o melhor deles o XGBoost com um f1-score de 0.85 e recall de 0.77

E finalmente, a útlima coisa a ser realizada foi a importância dos valores através do SHAP, sendo a coluna V14 e v4 as maiores influenciadoras na descoberta de fraudes.

Não foi realizada muitas mudanças nas quais o Expert fez pois achei a modelagem realizada quase perfeita. O único aprimoramento que foi realizado seria a conversão dos outliers para a média, e o treinamento e comparação de vários outros modelos, que mesmo assim, o XGBoost se tornou o melhor como a Expert mostra no vídeo

Comparando ao XGBoost treinado pela expert, houve um aprimoramento de 0.01 no f1-score e precisão do modelo por causa da transformação dos outliers.