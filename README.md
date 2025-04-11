# 🎧 Análise de Streaming Global no Spotify 2024 — MVP SQL

Projeto desenvolvido para o MVP da disciplina Ciência de Dados – PUC-RIO, utilizando a plataforma Databricks Community Edition e linguagem SQL pura.

## Objetivo

Construir um pipeline de dados em nuvem para responder perguntas de negócio reais com base nos dados de consumo musical global no Spotify em 2024. As questões abordadas são:

- Quais os artistas mais populares globalmente?
- Qual o gênero musical mais escutado?
- Quais países consomem mais músicas em termos de streams?
- Qual a média de streams por artista?
- Existe diferença significativa de consumo entre gêneros?

## Estrutura do Projeto

O projeto foi construído com base na arquitetura em camadas: Bronze → Silver → Gold

```txt
MVP ENG DADOS DUDABPF/
├── CSV/
│   └──1_spotify_2024.csv   
│
├── Evidencias/
│   ├── bronze_preview.png
│   ├── silver_preview.png
│   ├── gold_preview.png
│   ├── top10_artistas.png
│   ├── generos_populares.png
│   ├── paises_streams.png
│   ├── media_por_artista.png
│   └── media_por_genero.png
│
├── MVP - Maria Eduarda Battaglia - Estrutura da Entrega.pdf
└── README.md
```


## Camadas do Pipeline

### 🔸 Bronze  
Importação direta do arquivo CSV para o Databricks, sem tratamento.

### 🔸 Silver  
Limpeza dos dados, padronização de colunas, conversão de tipos e remoção de registros nulos.

### 🔸 Gold  
Agregações por artista, gênero e país com cálculo de métricas de negócio:
- Total de músicas
- Total de streams
- Média de streams por música

## Consultas de Análise

- `top10_artistas` — artistas com maior volume de streams
- `generos_populares` — gêneros mais escutados
- `paises_com_mais_streams` — países com mais consumo musical
- `media_streams_por_artista` — média de streams por artista
- `media_streams_por_genero` — comparação média entre gêneros

## Catálogo de Dados

O catálogo da camada Gold foi elaborado conforme exigência acadêmica, detalhando:
- Tipo de cada atributo
- Descrição
- Domínios esperados
- Qualidade dos dados
- Linhagem: origem, transformações, objetivos
---

## Licença

Este projeto está licenciado sob os termos da **Apache License 2.0**.

Isso significa que:

- Podendo **usar**, **copiar**, **modificar** e **redistribuir** este código livremente, inclusive para fins **acadêmicos**.
- Não há obrigação de tornar público seu código se o utilizar.
- É necessário manter os créditos e avisos de copyright originais.
- O projeto é fornecido **sem garantias**, sendo disponibilizado "no estado em que se encontra".

Para mais detalhes, consulte o texto completo da licença:  
[https://www.apache.org/licenses/LICENSE-2.0](https://www.apache.org/licenses/LICENSE-2.0)

👉 Ver seção “Modelagem” no relatório PDF

## Autoavaliação

Durante o desenvolvimento deste projeto, foram aplicados conceitos de engenharia de dados e análise SQL em nuvem. As principais dificuldades ocorreram na transformação do schema e adaptação dos dados para análise, superadas com apoio técnico. O projeto foi entregue completo, com todos os requisitos atendidos.

## Entrega

- Código estruturado por etapas
- Documentação completa (PDF)
- Notebook documentado
- Visualizações feitas diretamente no Databricks
- Prints organizados na pasta `/evidencias`

---

## Autoria

Maria Eduarda Battaglia Pedreira Fernandes  
PUC-Rio — Ciência de Dados  
Professor: Prof. Dr. Sérgio Lifschitz  
Abril de 2025

---


