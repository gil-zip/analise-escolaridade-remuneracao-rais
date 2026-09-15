# Dados

## Fonte

Os dados utilizados neste projeto são provenientes da Relação Anual de
Informações Sociais (RAIS) 2025, disponibilizada pelo Ministério do
Trabalho e Emprego.

A análise utiliza os microdados de vínculos do estado de São Paulo.

Arquivo original:

`RAIS_VINC_PUB_SP.COMT`

## Dados brutos

Os dados originais são armazenados localmente em:

`data/raw/`

O arquivo não é versionado no GitHub devido ao seu tamanho.

## Dados processados

O notebook `notebooks/01_preparacao_dados.ipynb` realiza a preparação
da base original e gera:

`data/processed/rais_sp_2025.parquet`

A base processada contém apenas os vínculos utilizados na população
analítica do projeto.

O arquivo Parquet também não é versionado devido ao seu tamanho e pode
ser reproduzido executando o notebook de preparação dos dados.

## População analítica

São considerados vínculos:

- ativos em 31/12/2025;
- com remuneração média nominal positiva;
- com escolaridade classificável;
- com atividade econômica classificável.

A unidade de análise é o vínculo formal de trabalho, e não o trabalhador
individual.