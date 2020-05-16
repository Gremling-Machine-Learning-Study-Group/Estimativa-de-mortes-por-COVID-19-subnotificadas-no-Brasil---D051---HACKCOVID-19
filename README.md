# Estimativa-de-mortes-por-COVID-19-subnotificadas-no-Brasil---D051---HACKCOVID-19
Parte 1 do desafio "IA E CIÊNCIA DE DADOS PARA APOIO A DECISÃO CLÍNICA" da Hackathon 'Hackcovid19' do Centro Brasileiro de Pesquisas Físicas, onde utilizamos conceitos simples de estatística, probabilidade e 'datascience' para tentar estimar a quantidade de casos de mortes por Síndrome Respiratória Aguda que foram causadas por COVID-19, porém não foram reportadas como tal.

Repositório Criado por: https://github.com/adsmendesdaniel

**Atenção:** Este é um modelo extremamente simples para tentar estimar os óbitos subnotificados, feito em curto espaço de tempo para uma Hackathon. Logo, um modelo mais sofisticado poderia ser criado para se alcançarem melhores resultados e, consequentemente, se obter uma melhor confiabilidade.

## ETAPA 1: Visualizar os dados:
  Os dados utilizados nesta parte do projeto são provenientes do site: 'https://bigdata-covid19.icict.fiocruz.br/', que é administrado pelo ICICT (Instituto de Comunicação e Informação Científica e Tecnológica em Saúde) e possui relações com a Fundação Oswaldo Cruz (Fiocruz). Estes dados, por ventura, são uma fração dos dadoss contidos na plataforma 'InfoGripe' da Fiocruz. (Olhar referências)
  Inicialmente, analisaremos o 'dataset' referente à mortes causadas por Síndrome Respiratória Aguda (SRAG) durante os anos 2018, 2019 e 2020 (até a 18ª semana epidemiológica). Donde podemos obter o sequinte gráfico:
  
  <p align="center">
  <img src="obitos_srag_semana_epidemiologica_brasil.png" align=middle height=250.973825pt/>
  </p>
  
## ETAPA 2: Estimar uma série temporal de mortes causadas por COVID-19 (junto a problemas advindos da pandemia) a partir dos dados anteriores:
  A metodologia foi obter médias dos casos (morte por SRAG) dos anos anteriores disponíveis (2018 e 2019) e gerar uma 'curva' para que, então, subtraiamos da 'curva' de mortes do ano decorrente (2020), e assim obtenhamos uma nova séries temporal de pontos correspondentes à uma estimativa de mortos por SRAG causada por COVID-19. Os resultados foram os seguintes:

  <p align="center">
  <img src="obitos_srag_semana_epidemiologica_brasil_media.png" align=middle height=250.973825pt/>
  </p>
  
  <p align="center">
  <img src="estimativa_obitos_covid_19.png" align=middle height=250.973825pt/>
  </p>

## ETAPA 3: Estimar mortes subnotificadas causadas por COVID-19:
  Podemos obters a aquantidade de mortes por SRAG esperadas por ano tomando a média dos pontos da curva de média de mortes dos anos 2018 e 2019. Fazendo o somatório dos valores da série temporal da média e dos casos de morte do ano de 2020 (até a 18ª semana epidemiológica) podemos obter a diferença, que corresponderá à uma estimativa do número de mortes causadas exclusivamente por fatores advindos do COVID-19.
  Nos 'datasets' disponibilizados por ICICT/Fiocruz podemos obter a quantidade de casos de morte por SRAG registradas como COVID-19. Então podemos calcular a diferença e obter uma estimativa para a quantidade de óbitos subnotificados de COVID-19, assim como sua devida porcentagem.
  Os dados obtidos em todo o processo são os seguintes:
  
  **Resultados:**
  Mortes decorrentes de SRAG esperadas por ano: 5403.0 

  Mortes decorrentes de SRAG até a 18ª semana epidemiológica: 1555.0 

  Estimativa de mortes decorrentes de COVID-19 até a 18ª semana epidemiológica: 18117.0 

  Óbitos confirmados por COVID-19 até a 18ª semana epidemiológica: 8547.0

  Estimativa de mortes por COVID-19 que não foram catalogadas como tal: 9570.0

  Porcentagem de mortes por COVID-19 subnotificadas: 52.8233151% 
  
## Referencias:
* **"MonitoraCovid-19** https://bigdata-covid19.icict.fiocruz.br/ (Visualizado em: 16/05/2020) (Daqui foram obtidos o dataset 'Casos de SRAG nos últimos anos' e 'Diagnósticos dos óbitos por SRAG').
* **InfoGripe** http://info.gripe.fiocruz.br/ (Visualizado em: 16/05/2020) (Donde os dados são divulgados originalmente. Daqui é possível obter datasets mais robustos com registros até o ano de 2009).
