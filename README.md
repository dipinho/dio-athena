# dio-athena

![alt text](https://blog-images.webscraper.io/images/3lKxthygrf8GBAE4drq6UmoqVR90LuQ6Y11GP3r6.png)

Repositório criado para o desafio de código do Bootcamp Ciências de Dados da DIO sobre o Amazon Athena.

<h2>Serviços utilizados</h2>
<li>Amazon S3</li>
<li>Amazon Glue</li>
<li>Amazon Athena</li>
<li>Amazon QuickSight</li>

<h2>Etapas para desenvolvimento</h2>

<h3>Criar bucket no Amazon S3</h3>
<li>Amazon S3 Console -> Buckets -> Create bucket -> Bucket name [nome_do bucket] - Create bucket</li>
<li>Create folder (Criar uma pasta chamada /output e outra com o nome do seu conjunto de dados. Este nome irá definir o nome da tabela criada no Glue)</li>
<li>Upload dos arquivos de dados localizados na pasta /data</li>

<h3>Criar Glue Crawler</h3>
<li>Amazon Glue Console -> Crawlers -> Add Crawler
<li>Source type [Data Stores] -> Crawl all folders
<li>Data store [S3] -> Include path [caminho do diretório dos dados de entrada]
<li>Create IAM Role
<li>Frequency [Run on demand]
<li>Database name [seu_nome_de_db]
<li>Group behavior [Create a single schema for each S3 path]
<li>Finish
<li>Databases -> Tables -> Visualizar dados das tabelas criadas

<h3>Criar aplicação no Amazon Athena</h3>
<li>Query editor -> Settings -> Manage settings -> Query result location and encryption -> Browse S3 -> selecionar o bucket criado
<li>Selecionar Database -> criar queries (exemplos na pasta /src)
<li>Verificar queries não salvas no bucket criado no S3
<li>Salavar queries -> Executar novamente -> Verificar no bucket criado no S3

<h3>Criando nova tabela</h3>
<li>Generate table DDL
<li>Copiar a query gerada
<li>Selecionar o DB e criar a nova tabela em uma nova query
<li>Visualizar dados no Amazon QuickSight
<li>Signup (caso não tenha conta) -> Escolher [Standard]
<li>Datasets -> Create new dataset -> Athena -> Name [NomeDoDataSet] -> Create
<li>Select database -> select table -> Edit or preview -> Save & visualize

<h3>Criar visualizações selecionando colunas, criando filtros e parâmetros e selecionando Visual types para gráficos.</h3>
