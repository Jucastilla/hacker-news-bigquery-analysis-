# Análise de Engajamento do Hacker News

## Contexto

Este projeto foi desenvolvido durante a formação em **Análise de Dados da EBAC**, a partir de uma atividade de aplicação de consultas SQL analíticas em uma base pública no **Google BigQuery**.

Foi utilizada a base do **Hacker News**, que reúne registros históricos de publicações, comentários e outros tipos de conteúdo da plataforma. No momento da análise, a tabela selecionada continha **49.299.014 registros**.

O ambiente foi configurado no **Visual Studio Code**, com integração ao **Google BigQuery** e desenvolvimento de um notebook para documentação do projeto.

A proposta original previa quatro consultas SQL. Para aprofundar a exploração dos dados, o projeto foi ampliado para **12 consultas**, documentadas com seus objetivos, recursos SQL utilizados e interpretação dos resultados.

## Objetivo

Analisar padrões de publicação e engajamento no Hacker News utilizando SQL e Google BigQuery, explorando indicadores relacionados a score, comentários, autores, domínios e comportamento temporal das publicações.

O projeto também teve como objetivo aplicar SQL em uma base pública de grande volume, desde a configuração do ambiente e exploração dos dados até a validação e documentação dos resultados.

## Desenvolvimento

### Configuração do Ambiente e Integração

O **Visual Studio Code** foi utilizado para elaboração e organização do notebook.

Foi realizada a integração com o **Google BigQuery**, incluindo a configuração do ambiente e das permissões necessárias para acessar a base pública.

As consultas foram desenvolvidas e testadas no BigQuery. O processo técnico, as consultas e as interpretações foram documentados no notebook.

### Fonte e Exploração dos Dados

Foi utilizada a tabela:

`bigquery-public-data.hacker_news.full`

Durante a exploração inicial, foram analisados:

- Estrutura e campos disponíveis;
- Esquema e tipos de dados;
- Volume de registros;
- Tipos de conteúdo;
- Presença de valores nulos;
- Variáveis relevantes para análise de publicação e engajamento.

Entre os principais campos utilizados estão `by`, `score`, `descendants`, `timestamp`, `url`, `type` e `id`.

### Desenvolvimento das Consultas SQL

Foram desenvolvidas **12 consultas analíticas**:

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

As consultas utilizaram:

- Filtros;
- Funções de agregação;
- Agrupamentos e ordenações;
- Funções de data e hora;
- Estruturas condicionais;
- JOINs;
- Cálculos derivados.

Cada consulta foi acompanhada de seu objetivo, dos principais recursos SQL utilizados e da interpretação dos resultados.

### Validação dos Dados e das Métricas

Foram realizadas verificações de valores nulos, possíveis duplicidades e consistência das métricas.

As consultas utilizaram filtros com `IS NOT NULL` quando as variáveis eram necessárias para os cálculos.

A verificação de duplicidades pelo campo `id` apresentou:

| Verificação | Resultado |
|---|---|
| Total de registros | 49.299.014 |
| IDs únicos | 49.299.014 |
| Possíveis duplicados por `id` | 0 |

Os resultados das consultas também foram comparados para verificar a coerência entre métricas, filtros e agrupamentos.

### Documentação e Exportação

O notebook reuniu a exploração inicial, a documentação da integração com o BigQuery, as consultas SQL, os procedimentos de validação e as interpretações.

Os resultados das 12 consultas foram exportados em formato CSV, organizados e padronizados de acordo com cada análise.

## Resultados

### Distribuição do Engajamento

A análise mostrou uma distribuição desigual do engajamento: a maior parte das publicações apresentou baixo score e poucos comentários, enquanto uma parcela menor concentrou níveis superiores de interação.

As publicações nas maiores faixas de score apresentaram médias de comentários significativamente superiores.

### Relação entre Comentários e Score

Foi observada uma associação entre a quantidade de comentários e o score das publicações. Conforme aumentou a quantidade de comentários, também aumentaram os valores médios e medianos de score.

Esse resultado representa uma associação observada nos dados e não implica uma relação causal.

### Padrões Temporais

Os períodos com maior volume de publicações não corresponderam necessariamente aos períodos de maior engajamento médio.

A análise histórica também identificou mudanças nos níveis de publicação e engajamento ao longo dos anos.

### Autores e Domínios

Foram identificadas diferenças de desempenho entre autores e domínios, distinguindo quantidade de publicações e engajamento obtido.

### Entregas do Projeto

O projeto resultou em **12 consultas SQL documentadas**, com resultados exportados em CSV e análises sobre publicação e engajamento em uma base de aproximadamente **49 milhões de registros**.

O desenvolvimento permitiu aplicar exploração, agregação, validação e interpretação de dados utilizando SQL no Google BigQuery, com documentação organizada em um notebook no Visual Studio Code.

## Habilidades Demonstradas

- Análise de dados;
- SQL;
- Google BigQuery;
- Google Cloud;
- Visual Studio Code;
- Jupyter Notebook;
- Integração com BigQuery;
- Exploração de dados;
- Validação de dados;
- Tratamento de valores nulos;
- Verificação de duplicidades;
- Agregação e agrupamento de dados;
- JOIN;
- CASE WHEN;
- Funções de data e hora;
- Funções de agregação;
- Cálculos derivados;
- Análise temporal;
- Análise de engajamento;
- Geração de insights;
- Documentação técnica.

## Arquivos do Projeto

Os arquivos estão organizados entre o notebook da análise e os resultados exportados das consultas.

### [Notebook — Análise de Engajamento do Hacker News](https://github.com/Jucastilla/hacker-news-bigquery-analysis-/blob/main/notebook/analise_hacker_news_bigquery.ipynb)

Notebook desenvolvido no Visual Studio Code, contendo a exploração inicial da base, a documentação da integração com o Google BigQuery, as 12 consultas SQL, os procedimentos de validação e a interpretação dos resultados.

### [Resultados das Consultas em CSV](https://github.com/Jucastilla/hacker-news-bigquery-analysis-/tree/main/data)

Pasta com os resultados das 12 consultas SQL exportados em formato CSV, organizados e padronizados de acordo com cada análise.
