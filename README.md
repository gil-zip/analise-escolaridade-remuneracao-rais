# Escolaridade e Remuneração no Mercado de Trabalho Brasileiro

Trabalho final desenvolvido para a disciplina de Ciência de Dados.

## Integrantes

- Giovani Andreoli — RA: 251020738
- Pablo Henrique Alves Pereira — RA: 251023575

## Tema

**Tema 3 — Mercado de trabalho: escolaridade e remuneração**

## Contexto

Decisões relacionadas à qualificação profissional dependem da compreensão da associação entre nível de escolaridade e remuneração no mercado de trabalho.

Este projeto investiga essa relação utilizando dados do mercado de trabalho formal do estado de São Paulo.

## Pergunta de pesquisa

**Como o nível de escolaridade está associado à remuneração dos trabalhadores formais do estado de São Paulo e como essa associação varia entre os setores de atividade econômica?**

## Objetivos

### Objetivo geral

Analisar a associação entre escolaridade e remuneração no mercado de trabalho formal paulista, verificando se essa relação varia entre diferentes setores de atividade econômica.

### Objetivos específicos

- Analisar a distribuição dos trabalhadores por nível de escolaridade.
- Comparar a remuneração entre diferentes níveis de escolaridade.
- Calcular o ganho salarial médio associado aos diferentes níveis educacionais.
- Comparar a relação entre escolaridade e remuneração entre setores econômicos.
- Investigar estatisticamente a associação entre escolaridade e remuneração.
- Discutir as limitações da análise e os fatores que podem influenciar a remuneração além da escolaridade.

## Fonte de dados

Será utilizada a **Relação Anual de Informações Sociais (RAIS)**, disponibilizada pelo Ministério do Trabalho e Emprego (MTE).

Ano-base inicialmente selecionado: **2025**.

Os microdados da RAIS contêm informações sobre vínculos formais de trabalho no Brasil, incluindo características do trabalhador, remuneração e atividade econômica.

Fonte oficial:

Ministério do Trabalho e Emprego — Programa de Disseminação das Estatísticas do Trabalho (PDET).

## Metodologia

O trabalho será desenvolvido nas seguintes etapas:

1. Obtenção e preparação dos dados.
2. Limpeza e tratamento dos microdados.
3. Análise Exploratória de Dados (EDA).
4. Estatística descritiva.
5. Análise da relação entre escolaridade e remuneração.
6. Comparação entre setores econômicos.
7. Análise de correlação.
8. Modelagem por regressão.
9. Discussão das limitações.
10. Elaboração da recomendação/conclusão final.

## Estrutura do projeto

```text
data/
├── raw/
└── processed/

figures/
notebooks/
report/
src/
```

* `data/raw`: dados originais.
* `data/processed`: dados tratados utilizados nas análises.
* `figures`: gráficos gerados pelo projeto.
* `notebooks`: notebooks Jupyter.
* `report`: materiais relacionados ao relatório final.
* `src`: funções e códigos auxiliares.

## Tecnologias

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Statsmodels