# Projeto de Análise de Dados | BigQuery

## Análise de Engajamento do Hacker News com SQL

## Sobre o Projeto

Este projeto foi desenvolvido durante a formação em Análise de Dados da EBAC, com o objetivo de aplicar consultas SQL analíticas no Google BigQuery utilizando uma base de dados pública.

O desenvolvimento foi realizado no **Visual Studio Code**, onde foi configurado o ambiente de trabalho e realizada a integração com o **Google BigQuery**, permitindo o acesso à base pública utilizada nas análises e o desenvolvimento do notebook que documenta todo o projeto.

Para a análise, foi utilizada a base pública do Hacker News disponível no BigQuery. O conjunto de dados reúne registros históricos de publicações, comentários e outros tipos de conteúdo da plataforma, permitindo investigar diferentes aspectos relacionados à atividade e ao engajamento da comunidade.

A proposta original da atividade envolvia o desenvolvimento de quatro consultas SQL analíticas. Como forma de aprofundar a exploração dos dados, o projeto foi ampliado para **12 consultas**, todas documentadas no notebook com seus objetivos, principais recursos SQL utilizados e interpretação dos resultados.

## Objetivo

Analisar padrões de publicação e engajamento no Hacker News utilizando SQL e Google BigQuery, explorando indicadores relacionados a score, comentários, autores, domínios e comportamento temporal das publicações.

O projeto também busca demonstrar a aplicação de SQL em uma base pública de grande volume, contemplando desde a configuração do ambiente e integração com o BigQuery até a exploração, análise, validação e documentação dos resultados.

## Etapas Desenvolvidas

### 1. Configuração do Ambiente e Integração com o BigQuery

O ambiente de desenvolvimento foi configurado no **Visual Studio Code**, utilizado para a elaboração e organização do notebook do projeto.

Foi realizada a integração com o **Google BigQuery**, garantindo o acesso ao ambiente do Google Cloud e à base pública utilizada na análise.

Após a configuração do ambiente e das permissões necessárias, as consultas SQL foram desenvolvidas e testadas no BigQuery, enquanto o processo técnico, as consultas e as interpretações dos resultados foram organizados e documentados no notebook.

### 2. Fonte e Exploração dos Dados

Foi utilizada a base pública:

`bigquery-public-data.hacker_news`

A tabela principal selecionada foi:

`full`

A tabela reúne registros históricos de diferentes tipos de conteúdo publicados no Hacker News.

Durante a exploração inicial, foram analisados:

- Estrutura e campos disponíveis;
- Esquema e tipos de dados;
- Volume de registros;
- Tipos de conteúdo;
- Presença de valores nulos;
- Variáveis relevantes para análise de publicação e engajamento.

No momento da análise, a tabela possuía **49.299.014 registros**.

Entre os principais campos utilizados estão `by`, `score`, `descendants`, `timestamp`, `url`, `type` e `id`.

### 3. Desenvolvimento das Consultas SQL

Foram desenvolvidas **12 consultas SQL analíticas**, abrangendo diferentes perspectivas sobre publicação e engajamento no Hacker News:

1. Distribuição dos tipos de conteúdo;
2. Publicações com maiores scores;
3. Indicadores gerais de engajamento;
4. Publicações com maior volume de comentários;
5. Engajamento por faixa de score;
6. Engajamento por dia da semana;
7. Engajamento por horário;
8. Autores com maior engajamento;
9. Evolução anual do engajamento;
10. Engajamento por dia da semana e horário;
11. Desempenho por domínio;
12. Relação entre comentários e score.

As consultas utilizaram recursos como filtros, agregações, agrupamentos, ordenações, funções de data e hora, estruturas condicionais, joins e cálculos derivados.

### 4. Análise dos Resultados

As consultas permitiram analisar o comportamento das publicações e do engajamento da comunidade sob diferentes perspectivas.

Entre os principais resultados observados:

- A maior parte das publicações apresenta baixo score e poucos comentários;
- Publicações pertencentes às maiores faixas de score apresentam médias de comentários significativamente superiores;
- A quantidade de comentários apresenta associação crescente com o score das publicações;
- Os períodos de maior volume de publicações não correspondem necessariamente aos períodos de maior engajamento médio;
- Foram identificadas diferenças de desempenho entre autores e domínios;
- A evolução histórica demonstra mudanças nos níveis de publicação e engajamento ao longo dos anos.

### 5. Validação dos Dados

Os resultados foram validados considerando consistência das métricas, presença de valores nulos e possíveis duplicidades.

Durante a exploração foram identificados valores nulos em diferentes campos. Por esse motivo, as consultas aplicaram filtros com `IS NOT NULL` quando as respectivas variáveis eram necessárias para os cálculos.

A verificação de duplicidades utilizando o campo `id` apresentou:

- **49.299.014 registros**;
- **49.299.014 IDs únicos**;
- **0 possíveis duplicados**.

Os resultados das diferentes consultas também foram comparados para verificar a coerência entre métricas, filtros e agrupamentos utilizados.

### 6. Conclusões

A análise demonstrou que o engajamento no Hacker News apresenta uma distribuição bastante desigual. A maior parte das publicações concentra baixos níveis de score e comentários, enquanto uma parcela menor alcança níveis significativamente superiores de interação.

Também foi observada uma associação entre comentários e score: conforme aumenta a quantidade de comentários, aumentam também os valores médios e medianos de score. Essa associação representa um padrão observado nos dados e não implica necessariamente uma relação causal.

As análises temporais mostraram que maior volume de publicações não significa necessariamente maior engajamento médio. Da mesma forma, as análises por autor e domínio demonstraram diferenças entre quantidade de publicações e desempenho.

De forma geral, o projeto permitiu trabalhar com uma base de aproximadamente **49 milhões de registros**, utilizando o Visual Studio Code integrado ao Google BigQuery para desenvolver, validar e documentar consultas SQL capazes de transformar os dados históricos em indicadores sobre o comportamento e o engajamento da comunidade.

## Habilidades Demonstradas

- Análise de Dados
- SQL
- Google BigQuery
- Google Cloud
- Visual Studio Code
- Jupyter Notebook
- Integração com BigQuery
- Exploração de Dados
- Validação de Dados
- Tratamento de Valores Nulos
- Verificação de Duplicidades
- Agregação e Agrupamento de Dados
- JOIN
- CASE WHEN
- Funções de Data e Hora
- Funções de Agregação
- Cálculos Derivados
- Análise Temporal
- Análise de Engajamento
- Geração de Insights
- Documentação Técnica

## Arquivos do Projeto

Os arquivos desenvolvidos estão organizados de acordo com as diferentes etapas da análise.

### Notebook

📓 [Notebook - Análise de Engajamento do Hacker News](COLE_AQUI_O_LINK_DO_NOTEBOOK)

Notebook desenvolvido no Visual Studio Code, contendo a exploração inicial da base, documentação do ambiente e integração com o Google BigQuery, as 12 consultas SQL, validação dos dados e interpretação dos resultados.

### Consultas SQL

💻 [Acessar Consultas SQL](COLE_AQUI_O_LINK_DA_PASTA_SQL)

A pasta reúne as 12 consultas SQL desenvolvidas no projeto, organizadas e nomeadas de acordo com o objetivo de cada análise.

### Resultados das Consultas

📊 [Acessar Resultados em CSV](COLE_AQUI_O_LINK_DA_PASTA_DATA)

A pasta contém os resultados das 12 consultas SQL exportados em formato CSV, mantendo a organização e a padronização utilizadas durante a análise.
