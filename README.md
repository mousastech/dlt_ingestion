<img src="https://github.com/mousastech/dlt_ingestion/blob/b41541716757c8fe197dfd35ee74d97af4c85399/files/DLT%20Ingest.png?raw=true">

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
- Para criar os catálogos utilize os comandos abaixo: 

<code>
CREATE CATALOG ecommerce; 
USE catalog ecommerce;
CREATE SCHEMA bronze;
CREATE SCHEMA silver;
CREATE SCHEMA gold;
</code>

<br>
- Após criar o catálogo, criar uma Externa Location:
<br><br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/e96c8bc75e87f992d806f650b08c21c72412b818/files/3.Create_External_data.gif?raw=true">

<br><br>
- Criar um Volume do tipo Externo:
<br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/f834853775a4199cdabaa09c4bdedfe0ed7edf1b/files/2.CreateVolume.png?raw=true">

<br>
Disponível no notebook <code>setup.ypnb</code>
<br><br>
<b> Estrutura dos arquivos no Storage Account AWS S3</br>
<img src="https://github.com/mousastech/dlt_ingestion/blob/8ce6c705986446bd3adae12dc67a7dce2e37f55f/files/1.Estrutura%20S3.gif?raw=true">

<b>Talk to me:</b>

[![Linkedin Badge](https://img.shields.io/badge/-Moises-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/rochamoises/)](https://www.linkedin.com/in/rochamoises/) 
[![Gmail Badge](https://img.shields.io/badge/-mousas.rocha@gmail.com-c14438?style=flat-square&logo=Gmail&logoColor=white&link=mailto:mousas.rocha@gmail.com)](mailto:mousas.rocha@gmail.com)
