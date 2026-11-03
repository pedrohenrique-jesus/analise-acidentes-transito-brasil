# 🚗 Análise de Acidentes de Trânsito no Brasil

## 📌 Sobre o Projeto

Este projeto tem como objetivo analisar os acidentes de trânsito nas rodovias federais brasileiras, utilizando dados públicos da Polícia Rodoviária Federal (PRF), a fim de identificar padrões, fatores de risco e oportunidades de prevenção.

---

## 🎯 Objetivo

Fornecer insights baseados em dados que contribuam para a compreensão dos acidentes de trânsito no Brasil, apoiando a tomada de decisão e possíveis ações de mitigação.

---

## 🗂️ Fonte de Dados

Os dados utilizados foram obtidos da Polícia Rodoviária Federal, por meio do portal de dados abertos
(https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf).

* Tipo: Dados estruturados (CSV)
* Conteúdo: Informações sobre acidentes, localização, causas, condições e vítimas

* **Período dos registros:** Ano de 2025
* **Quantidade de registros:** 142.770 linhas
* **Quantidade de variáveis:** 37 colunas

---

## 🛠️ Tecnologias Utilizadas

* Python (Pandas, Matplotlib)
* Google Colab
* Looker Studio
* GitHub

---

## 🔍 Etapas do Projeto

### 1. Definição do Problema

Análise da relevância dos acidentes de trânsito como problema de segurança pública e identificação de hipóteses investigativas.

### 2. Coleta de Dados

Levantamento de dados públicos disponibilizados pela PRF.

### 3. Análise Exploratória (EDA)

* Limpeza e tratamento dos dados
* Criação de variáveis (ex: gravidade)
* Análise por tempo, localização e causas

### 4. Geração de Insights

Principais descobertas:

* Maior concentração de acidentes às 18h, seguida por 17h, 7h e 19h.
* Predominância de causas relacionadas à reação dos condutores, com destaque para reação tardia ou ineficiente e ausência de reação.
* Minas Gerais, Paraná e Santa Catarina apresentam os maiores volumes de acidentes entre os estados destacados no dashboard.

### 5. Visualização de Dados

Dashboard interativo desenvolvido no Looker Studio:

👉 (https://datastudio.google.com/reporting/507e42a2-effd-421b-886a-57c8059ce0ec)

---

## Principais Resultados e Interpretações

### 1. Concentração de acidentes nos horários de pico

**O que foi identificado:** Os acidentes apresentam maior concentração no período da tarde, com destaque para o horário das 18h.

**Evidência:** O gráfico de distribuição de acidentes ao longo do dia aponta 18h como o horário com maior número de ocorrências, seguido por 17h, 7h e 19h.

**Interpretação:** A concentração nesses horários indica uma maior ocorrência de acidentes em períodos de deslocamento intenso, como os horários de entrada e saída do trabalho.

**Limitação:** Os dados mostram a distribuição dos acidentes por horário, mas não permitem afirmar que o fluxo de veículos seja a causa direta desse comportamento, nem calcular o risco individual de acidente em cada horário.

### 2. Predominância de causas relacionadas à reação dos condutores

**O que foi identificado:** As categorias relacionadas à reação dos condutores aparecem entre as principais causas registradas nos acidentes analisados.

**Evidência:** A reação tardia ou ineficiente do condutor representa aproximadamente 16,7 mil registros, enquanto a ausência de reação do condutor aparece em segundo lugar, com aproximadamente 14,5 mil. A velocidade incompatível ocupa a terceira posição, com aproximadamente 10,8 mil.

**Interpretação:** Os resultados destacam a relevância dos fatores relacionados à atenção, à capacidade de reação e à condução em velocidade adequada no contexto dos acidentes registrados.

**Limitação:** A classificação das causas permite identificar os fatores registrados pela PRF, mas não comprova, isoladamente, as circunstâncias individuais de cada ocorrência nem estabelece relações causais além do que os dados permitem observar.

### 3. Concentração de acidentes em determinados estados

**O que foi identificado:** Minas Gerais, Paraná e Santa Catarina apresentam os maiores volumes de acidentes entre os estados destacados no dashboard.

**Evidência:** Minas Gerais registra aproximadamente 16,4 mil acidentes, seguido pelo Paraná, com 14,1 mil, e Santa Catarina, com 10,2 mil.

**Interpretação:** A distribuição evidencia uma concentração de ocorrências nesses estados, indicando regiões que merecem atenção em análises de segurança viária e planejamento de ações preventivas.

**Limitação:** O volume absoluto de acidentes não representa, por si só, o risco de ocorrência. Para comparar o risco entre estados, seria necessário considerar fatores como fluxo de veículos, extensão da malha rodoviária e volume de deslocamentos.

**Nota metodológica:** A variável `gravidade` foi definida como a soma de vítimas fatais (`mortos`) e vítimas gravemente feridas (`feridos_graves`). A taxa de gravidade por estado corresponde à divisão dessa soma pela quantidade de registros considerados na análise, não representando diretamente a porcentagem de acidentes graves.

---

OBS: Devido às limitações de ferramentas de visualização, foi realizada uma amostragem e seleção de variáveis para otimizar o desempenho do dashboard, mantendo a representatividade dos dados.

---

### Metodologia e interpretação dos indicadores

A base disponibilizada pela Polícia Rodoviária Federal (PRF) contém registros relacionados aos acidentes e às pessoas envolvidas. Para garantir uma interpretação adequada dos resultados, foram considerados os seguintes conceitos:

- **Quantidade de acidentes:** contabilizada por meio da contagem de identificadores (`id`), representando as ocorrências registradas na base.
- **Pessoas envolvidas:** os registros da base também contêm informações sobre os participantes dos acidentes. Dessa forma, a quantidade de linhas não necessariamente corresponde à quantidade de ocorrências, pois um acidente pode envolver várias pessoas.
- **Gravidade:** considera os registros de vítimas fatais (`mortos`) e feridas gravemente (`feridos_graves`), conforme os critérios utilizados nas análises.

Essa distinção permite interpretar corretamente os indicadores apresentados no dashboard, diferenciando o volume de acidentes da quantidade de pessoas envolvidas e da gravidade das ocorrências.

## 🚀 Conclusão

A análise permitiu identificar padrões temporais, geográficos e causas registradas nos acidentes ocorridos nas rodovias federais brasileiras em 2025. Os resultados destacam a concentração de ocorrências em determinados horários e estados, além da relevância das causas relacionadas à reação dos condutores. O uso de dados possibilitou transformar registros públicos em informações que podem contribuir para a compreensão do cenário da segurança viária e apoiar discussões sobre ações preventivas.

---

## 👤 Autor

Pedro Henrique Correia de Jesus

Projeto desenvolvido para fins de estudo e portfólio em análise de dados.

