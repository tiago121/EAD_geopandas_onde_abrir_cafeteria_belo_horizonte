# EAD_geopandas_onde_abrir_cafeteria_BH

#### Made by Tiago Araujo

# Descrição

Esse projeto coleta dados do IBGE e faz webscraping para conseguir dados demográficos/geográficos e recomendar o melhor local para se abrir uma cafeteria na cidade de Belo Horizonte.

# 1. Problema de negócio

Empresário do ramo alimentício precisa de informações para decidir a escolha da abertura de um negócio em Belo Horizonte. Para que o negócio seja rentável, precisa trazer uma média de 150 clientes por dia, consumindo em média de 50 reais cada. 

O projeto a seguir ajuda na análise de critérios objetivos para descobrir qual o local mais adequado, fazendo recomendações finais ao gestor.

# 2. Estratégia de solução


**Etapa 01. Coleta dos dados**

Nesse projeto, trabalhei com os seguintes dados:

- Dados demográficos (renda, faixa_etária e densidade)
- Dados de geolocalização de Belo Horizonte
- Endereços de cafeterias na cidade

Os dados foram coletados do Censo de 2010, do site da prefeitura de Belo Horizonte e do site Apontador (esse por meio de webscraping).
Os dados foram transformados em geográficos para visualização.


**Etapa 02. Descrição, limpeza  e filtragem de dados**

* Objetivo: Entender e selecionar o recorte adequado de dados para análise.
* Processo: Pré-processamento de dados no Excel para filtrar dados de acordo com o percentual de público alvo de cafeterias por bairro; preenchimento de dados faltantes e junção das bases.


**Etapa 03. Plotagem de mapas**

* Objetivo: visualizar, geograficamente, onde estão as maiores oportunidades de negócio de acordo com a renda, a faixa etária e a densidade dos bairros.
* Processo: Uso de geopandas e matplotlib para fazer os mapas, assim como funções que indicam os locais mais propícios.

Exemplo de mapa gerado:
![image](https://user-images.githubusercontent.com/88745881/232543310-b4006011-530b-41b9-9ebf-d95a1c096962.png)


**Etapa 04. Criação de ranking de bairros**

* Objetivo: Ter um parâmetro objetivo de escolha
* Processo: Normalização dos dados e criação de variável com média ponderada com renda, faixa etária e densidade (dando peso maior para as duas primeiras) e plotagem em gráfico de pontos


**Etapa 05. Plotagem de potenciais concorrentes ao longo da cidade**

* Objetivo: identificar possíveis concorrentes nas regiões
* Processo: usar dados de endereços via webscraping, transformar endereços em coordenadas geográficas, limpar os dados e plotar, fazendo a comparação entre os melhores bairros e a concorrência.

![image](https://user-images.githubusercontent.com/88745881/232543732-15b72f59-5e0b-404e-b438-d2ef712166ae.png)


# 3. Conclusão e recomendações finais

* Objetivo: Fazer um resumo do projeto e quais as ações recomendação ao gestor, a partir das análises feitas

Recomendações:

- Há elevada discrepância entre as regiões e vários locais com boas oportunidades, sendo os 20 principais rankeados
![image](https://user-images.githubusercontent.com/88745881/232542703-e09484a3-3325-47f1-be9e-0059932a970a.png)



- O bairro que apresentou as melhores condições/oportunidades foi o Boa Viagem

![image](https://user-images.githubusercontent.com/88745881/232540239-adef8344-ed02-4ce0-8d0f-f251be01cbdb.png)


# 4. Limitações e próximos passos

**Limitações:**

- As informações sobre bairros estão defasadas, já que o último censo foi feito em 2010; é necessário atualizar os dados assim que o novo estiver pronto (previsto para conclusão esse ou ano que vem);
- Houve várias informações faltantes no arquivo do IBGE que não poderiam ser imputadas.

**Algumas outras análises podem ser feitas para melhorar os resultados obtidos:**

- Análise dos custos fixos e variados associados ao bairro;
- Análise de dados de gênero e desemprego;
- Comparações entre capitais.
