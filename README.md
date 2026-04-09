# Trabalho Balão — Criminalidade e Meteorologia em Passo Fundo/RS

## Integrantes

- Bruno Gonçalves de Oliveira — 1135895
- João Pedro Pereira — 1135923
- Pedro Luis Alves Bartz — 1135935
- Pedro Rodolfo de Araujo Rien — 1136094
- Rafael Scortegagna Pedra — 1136090
- Ricardo Zanandrea — 1136748

## Repositório

[https://github.com/rafascort/trabalhobalao](https://github.com/rafascort/trabalhobalao)

## Sobre o projeto

Realizado um pipeline completo de análise de dados envolvendo criminalidade e condições meteorológicas no município de Passo Fundo/RS entre 2021 e 2026. O processo é dividido em cinco etapas: leitura e filtragem dos arquivos originais de boletins de ocorrência (seis arquivos anuais em CSV), concatenação e padronização das colunas, limpeza e tratamento de valores ausentes e inconsistências categóricas, integração com dados meteorológicos diários da estação A839 do INMET via merge por data, e por fim transformações que incluem redução de cardinalidade de variáveis categóricas, label encoding, detecção e capping de outliers pelo método IQR e normalização das variáveis numéricas (min-max para dados climáticos e z-score para dados de crime). O resultado final é o arquivo `df_final.csv`, um dataset unificado e tratado contendo registros de crimes de Passo Fundo associados às condições climáticas do dia do fato, com variáveis codificadas e normalizadas, pronto para uso em análises estatísticas e modelos de machine learning.

## Estrutura do repositório

```
trabalho balao/
├── crimes/
│   ├── teste.ipynb              # Etapas 1, 2 e 3 — leitura, concatenação e limpeza dos dados de criminalidade
│   ├── crime_2021.csv           # Arquivo original — boletins de ocorrência 2021
│   ├── crime_2022.csv           # Arquivo original — boletins de ocorrência 2022
│   ├── crime_2023.csv           # Arquivo original — boletins de ocorrência 2023
│   ├── crime_2024.csv           # Arquivo original — boletins de ocorrência 2024
│   ├── crime_2025.csv           # Arquivo original — boletins de ocorrência 2025
│   ├── crime_2026.csv           # Arquivo original — boletins de ocorrência 2026
│   └── CrimesTratados.csv       # Arquivo final — crimes tratados e padronizados
├── meteorologia/
│   ├── testeMet.ipynb           # Etapas 4 e 5 — integração meteorológica e transformações
│   ├── jan21_ago25.csv          # Arquivo original — dados meteorológicos Jan/2021–Ago/2025
│   ├── dados_A839_D_2025-09-01_2026-04-06.csv  # Arquivo original — dados meteorológicos Set/2025–Abr/2026
│   └── df_final.csv             # Arquivo final — dataset unificado, tratado e pronto para análise
└── README.md
```
