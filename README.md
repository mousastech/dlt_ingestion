<img src="https://github.com/mousastech/dlt_ingestion/blob/1d1acf88ef16711f398e202ea703b6c3336765e9/files/DLT%20Ingest.png?raw=true">

# Project
Import data from AWS S3 through the Unity Catalog using Delta Live Tables.

# Structure 

<b>1. Conectar a um storage Account (AWS S3) através de uma External Location: mostrar como se conecta a um storage account através do Unity Catalog </b>
- Usar Cloud Formation da AWS para configurar mas facilmente
- Revisar External Data → Credentials → External Locations 

<b>2. Criar securable objects do Unity catalog para governar os dados:</b>
- Criar Catálogo → Esquema → Volume (External)
- Reflexões sobre melhor estratégia de organização dos dados

<b>3. Create sample pipeline → apresentar conceitos e mostrar principais funcionalidades do pipeline gerado </b>
- Mostrar diferenças entre o DLT tradicional e DLT SaaS

<b>4. Criar um pipeline de dados do zero usando Delta Live Tables </b>
- Apresentação da arquitetura
- Definição das tabelas 
- Criação do pipeline 

# Architecture 

<br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/310a653f53e200c1be2547cdb090c4135196c6a4/files/0.Demo_Architecture.png?raw=true">
<br><br>

<img src="https://github.com/mousastech/dlt_ingestion/blob/69f95cedbea4e6e570e62861b4924b5242659458/files/1.Storage_Logical.png?raw=true">

<br>

# Hands-on 

<b>1 - Executar notebook</b> <code> ./Setup </code>

Ou obter o detalhe abaixo:
<br>

<code>CREATE CATALOG ecommerce; 
USE catalog ecommerce;
CREATE SCHEMA bronze;
CREATE SCHEMA silver;
CREATE SCHEMA gold;
</code>

<br>
<b>2 - Criar External Location:</b>
<br><br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/e96c8bc75e87f992d806f650b08c21c72412b818/files/3.Create_External_data.gif?raw=true">

<br><br>
<b>3 - Criar um Volume do tipo Externo:</b>
<br><br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/f834853775a4199cdabaa09c4bdedfe0ed7edf1b/files/2.CreateVolume.png?raw=true">

<br>
Disponível no notebook <code>setup.ypnb</code>
<br><br>
<b> 4 - Carregar arquivos no Storage Account AWS S3</b><br><br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/8ce6c705986446bd3adae12dc67a7dce2e37f55f/files/1.Estrutura%20S3.gif?raw=true">

<br><br>
<b>5 - Abrir notebook:</b> <code> Ingest DLT ecommerce.ipynb </code> 
<br>

<br><br>
<b>6 - No meu Data Engineering -> Delta Live Tables: Create Pipeline</b><code>
<br><br>

<img src="https://github.com/mousastech/dlt_ingestion/blob/72c9b97b12799ce52b449c59bdc94dd21539dce0/files/Parte%205%20-%20Criar%20Pipeline.gif?raw=true">

<br><br>
<b>7 - Conferir resultado do Pipeline e revisar funções</b>
<br><br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/6f39ec4b39a3a88297975b816022dbc57cc770c5/files/4.DLT_Pipeline.png?raw=true">

<br><br>
<b>8 - Abrir notebook:</b> <code>Data Ingestion Traditional.ipynb</code> e executar para fins de comparação
<br><br>

<img src="https://github.com/mousastech/dlt_ingestion/blob/8fe4037d2be4579233854956e415cbb69708dc9c/files/5.Traditional.png?raw=true">
<br><br>

Dúvidas? Comentários? Sugestões e críticas, são apreciados.


<br><br>
<b>Talk to me:</b>

[![Linkedin Badge](https://img.shields.io/badge/-Moises-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/rochamoises/)](https://www.linkedin.com/in/rochamoises/) 
[![Gmail Badge](https://img.shields.io/badge/-mousas.rocha@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:mousas.rocha@gmail.com)](mailto:mousas.rocha@gmail.com)
