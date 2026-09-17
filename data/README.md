# Dados

## Fonte

Os dados utilizados neste projeto são provenientes da Relação Anual de
Informações Sociais (RAIS) 2025, disponibilizada pelo Ministério do
Trabalho e Emprego.

A análise utiliza os microdados de vínculos do estado de São Paulo.

Arquivo original:

`RAIS_VINC_PUB_SP.COMT`

Data de download: 14/09/2026.

## Como obter os dados

O acesso aos microdados é feito via FTP:

`ftp://ftp.mtps.gov.br/pdet/microdados/`

Navegadores modernos (Chrome, Edge, Brave, Firefox) não suportam mais o
protocolo FTP. O acesso pode ser feito por:

- Windows Explorer: `Win + E`, colar o endereço acima na barra de
  endereços e pressionar Enter;
- um cliente FTP dedicado (ex.: FileZilla), caso o método acima falhe.

O arquivo é disponibilizado compactado em `.7z`. Após o download, deve
ser extraído com o WinRAR ou 7-Zip e o resultado movido para
`data/raw/`, mantendo o nome `RAIS_VINC_PUB_SP.COMT` diretamente dentro
dessa pasta (sem subpastas).

## Formato do arquivo

- Delimitador: `,` (campos entre aspas duplas — padrão CSV)
- Encoding: latin1
- Confirmado via inspeção da primeira linha do arquivo após extração.

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