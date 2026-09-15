# Escolaridade e Remuneração no Mercado de Trabalho Formal de São Paulo

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

- Analisar a distribuição dos vínculos formais por nível de escolaridade.
- Comparar a remuneração entre diferentes níveis de escolaridade.
- Calcular as diferenças de remuneração associadas aos diferentes níveis educacionais.
- Comparar a relação entre escolaridade e remuneração entre setores econômicos.
- Investigar estatisticamente a associação entre escolaridade e remuneração.
- Discutir as limitações da análise e os fatores que podem influenciar a remuneração além da escolaridade.

## Fonte de dados

O projeto utiliza os microdados da **Relação Anual de Informações Sociais (RAIS)**, disponibilizados pelo **Ministério do Trabalho e Emprego (MTE)** por meio do Programa de Disseminação das Estatísticas do Trabalho (PDET).

- **Ano-base:** 2025
- **Unidade da Federação:** São Paulo
- **Arquivo utilizado:** `RAIS_VINC_PUB_SP.COMT`
- **Data de download:** 14/09/2026
- **Fonte:** Ministério do Trabalho e Emprego — PDET
- **Acesso aos microdados:** `ftp://ftp.mtps.gov.br/pdet/microdados/`

A RAIS é um registro administrativo anual que reúne informações sobre estabelecimentos e vínculos formais de trabalho. Neste projeto, a unidade de análise é o **vínculo formal de trabalho**, e não o trabalhador individual.

O arquivo original possui aproximadamente 6,37 GB e, por esse motivo, não é versionado no repositório.

## População analisada

A análise é restrita aos vínculos formais do estado de São Paulo presentes nos microdados da RAIS 2025.

Durante a preparação dos dados, são considerados para a base analítica os vínculos:

- ativos em 31/12/2025;
- com remuneração média nominal positiva;
- com nível de escolaridade classificável;
- com atividade econômica classificável.

A atividade econômica é agrupada em cinco grandes setores a partir da CNAE 2.0:

- Agropecuária;
- Indústria;
- Construção;
- Comércio;
- Serviços.

Após o processamento, a base analítica resultante contém **14.948.065 vínculos formais**.

## Metodologia

O trabalho é desenvolvido nas seguintes etapas:

1. Obtenção e documentação dos microdados da RAIS 2025.
2. Seleção e tratamento das variáveis relevantes.
3. Preparação da base analítica.
4. Análise Exploratória de Dados (EDA).
5. Estatística descritiva.
6. Análise da relação entre escolaridade e remuneração.
7. Comparação entre setores econômicos.
8. Análise estatística e modelagem por regressão.
9. Discussão das limitações e possíveis fatores de confusão.
10. Elaboração das conclusões e recomendações finais.

A análise é observacional. Portanto, os resultados são interpretados como **associações entre escolaridade e remuneração**, não como evidência de uma relação causal.

## Estrutura do projeto

```text
analise-escolaridade-remuneracao-rais/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── README.md
│
├── docs/
├── figures/
├── notebooks/
├── report/
├── src/
│
├── .gitignore
├── README.md
└── requirements.txt
```

- `data/raw`: microdados originais da RAIS, não versionados.
- `data/processed`: dados tratados utilizados nas análises, não versionados.
- `data/README.md`: documentação específica sobre os dados.
- `docs`: documentação oficial da RAIS e da CNAE utilizada no projeto.
- `figures`: gráficos e visualizações gerados pelo projeto.
- `notebooks`: notebooks Jupyter utilizados na preparação e análise dos dados.
- `report`: materiais relacionados ao relatório final.
- `src`: funções e códigos auxiliares.

## Dados processados

A preparação dos dados é realizada no notebook:

```text
notebooks/01_preparacao_dados.ipynb
```

A base resultante é armazenada em:

```text
data/processed/rais_sp_2025.parquet
```

O arquivo processado possui aproximadamente 298 MB e não é versionado no GitHub. Ele pode ser reproduzido a partir dos microdados originais executando o notebook de preparação.

## Tecnologias

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- PyArrow

## Reprodutibilidade

As dependências utilizadas no projeto estão disponíveis em:

```text
requirements.txt
```

Após configurar o ambiente Python e instalar as dependências, os notebooks podem ser executados seguindo sua ordem numérica.

Os arquivos brutos e processados não são armazenados no GitHub devido ao seu tamanho.