# Estudo de modelos preditivos para prever doenças cardíacas.
<br>
Trata-se de estudo no qual os códigos e dados foram extraídos do site kaggle.com realizado com finalidade de aprendizagem.
Com esse intuito, realizei a edição de cada etapa, estudando, analisando e comentando.
<br>
1) Inicialmente foram utilizados os dados relativos ao coração de vários indivíduos, constando as seguintes informações:
<pre>
a) Age: idade do paciente (em anos)
b) Sex: Sexo (M ou F)
c) ChestPainType: Tipos de dores no peito (TA: dores típicas, ATA: Dores atípicas, NAP: sem dores, ASY: assintomáticos)
d) RetingBP: Pressão sanguínea em repouso (mm Hg)
e) Cholesterol: Colesterol (mm/dl)
f) FastingBS: Açucar no sangue em jejum (1 se acima de 120 ou 0 se abaixo)
g) RestingECG: Resultado eletrocardiograma em jejum (Normal: Normal, ST: anormal, LVH: provável hipertrofia ventricular esquerda)
h) MaxHR: frequência cardíaca máxima (de 60 a 202)
i) ExeciseAngina: Dores no peito induzida por exercícios (Y: sim, N: não)
j) Olpeak: Depressão de ST induzida por execício em relação ao repouso ( ST é uma medida obtida no eletro cardiograma) 
k) ST_Slope: Inclinação do seguimento ST de pico do exercício ( ST é uma medida obtida no eletro cardiograma). (Up: ascendente, Flat: normal, Down: descendente)
l) HeartDisease: possui ou não doenças cardíacas (1: possui, 0: não possui)
</pre>
<br>
2) Processo de extração e análise dos dados. Foram realizados:
<pre>
a) Verificação de dados nulos
b) exploração dos dados com pandas profiling
</pre>
<br>
3) Pre-precessamento dos dados:
<pre>
a) tranformação dos dados alfanuméricos em dados numéricos 
b) Dimensinamento dos dados para valores entre -1 e 1
c) Seleção dos dados relevantes 
d) Retirada de dados pouco relevantes. Utilizando-se da biblioteca SelectKBest verificou-se que o dados RetingECG e RestingBP eram pouco relevantes para predição de doenças cardíacas.
</pre>
<br>
4) Extração dos melhores parâmetros de cada modelo com impressão da métrica de avaliação do modelo "ROC AUC", sendo eles:
<pre>
a) Support Vector Machine
b) KNeighborsClassifir
c) MLP
d) Random Forest
e) XGBoost
f) CatBoost
g) AdaBoost
h) Decision tree
i) Naive Bayes
j) Logistic Regression
k) LightGBM
</pre>
<br>
5) Criação de modelo por empilhamento utilizando os melhores parâmetros de cada um dos modelos anteriormente testados.
6) Obtenção da classificação de cada um dos modelos com base no "ROC AUC" incluindo o modelo obtido pelo empilhamento que foi nomeado de "stacking", e apresentação gráfica boxplot:

<img src="https://github.com/AdilsonBND/predicao-doencas-cardiacas/blob/main/images/output.png"></img>
