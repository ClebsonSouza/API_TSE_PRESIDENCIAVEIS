# API_TSE_PRESIDENCIAVEIS
# Eleições 2026 | Análise e Visualização de Dados com Python

## Sobre o projeto

Este projeto utiliza **Python** para consultar, processar e visualizar os resultados das eleições presidenciais de 2026, a partir de dados disponibilizados pelo **Tribunal Superior Eleitoral (TSE)**.

A aplicação realiza consultas a arquivos JSON do portal oficial de resultados, organiza as informações em um DataFrame do Pandas e apresenta os resultados por meio de gráficos profissionais, permitindo acompanhar a distribuição dos votos entre os candidatos.

## Tecnologias utilizadas

- **Python:** linguagem utilizada no desenvolvimento.
- **Requests:** consulta aos dados disponibilizados pelo TSE.
- **Pandas:** tratamento, organização e análise dos dados.
- **Matplotlib:** construção e personalização dos gráficos.

## Funcionalidades

- Consulta automatizada aos resultados oficiais das eleições.
- Extração de informações dos candidatos, partidos e votações.
- Organização dos resultados em um DataFrame.
- Conversão e formatação de valores numéricos e percentuais.
- Ordenação dos candidatos pela quantidade de votos.
- Visualização em gráficos de barras horizontais.
- Destaque visual para o candidato com maior votação registrada.
- Adaptação dos gráficos aos dados do primeiro e segundo turnos.

## Estrutura dos dados

| Coluna | Descrição |
|---|---|
| `numero` | Número eleitoral do candidato. |
| `nome` | Nome completo do candidato. |
| `nome_urna` | Nome utilizado na urna eletrônica. |
| `partido` | Sigla do partido político. |
| `votos` | Quantidade de votos recebidos. |
| `percentual` | Percentual de votos válidos. |
| `situacao` | Situação eleitoral do candidato. |
| `eleito` | Indicador de eleição ou classificação retornado pelo TSE. |

## Configuração da consulta

O projeto permite selecionar o turno da eleição por meio da variável `codigo_eleicao`:

```python
codigo_eleicao = 6257  # Primeiro turno
codigo_eleicao = 6258  # Segundo turno
```

A URL de consulta é construída dinamicamente, permitindo utilizar a mesma estrutura de código para ambos os turnos.

## Visualização dos resultados

Os resultados são apresentados em gráficos de barras horizontais, desenvolvidos com Matplotlib, contendo:

- Paleta de cores com fundo escuro e alto contraste.
- Destaque em dourado para a maior votação registrada.
- Identificação dos candidatos.
- Rótulos com percentuais e quantidade de votos.
- Ajuste automático da altura conforme o número de candidatos.

A visualização permite comparar os resultados de maneira objetiva, facilitando a identificação das diferenças de votação entre os candidatos.

## Fonte dos dados

Os dados são obt
