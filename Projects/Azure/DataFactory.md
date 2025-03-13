# Azure Data Factory

In Azure, a pipeline was created with Data Factory to retrieve data from a SQL database, and export the data to a CSV file on a storage account. The exported CSV file is then transformed with a filter to generate another CSV file.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/SQLToBlob.png"/></p>

<p>
The following Azure resources are created in the East 2 zone.
<ol>
<li>SQL database</li>
<li>Storage account</li>
<li>Data Factory</li>
</lo>
</p>
  
## SQL database
When creating a SQL database, a server needs to be created if one does not already exist. 
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/CreateDatabase.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DBCreationForm.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DBServerForm.png"/></p>
For authentication, SQL and Microsoft Entra Authentication are enabled. 

The database will have tables created with data. This was done within VS Code.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/VSCodeCreateTables.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/VSCodeInsertData.png"/></p>

## Storage account
When creating a storage account, a container needs to be created. This is where the data will be exported to.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/StorageandContainer.png"/></p>

## Data Factory
Creating a Data Factory is similar to creating other resources, for which a name and resource group need to be selected.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/CreateDataFactor.png"/></p>
Click on Data Factory Studio to continue.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFactoryStudio.png"/></p>
Select Ingest to ingest data.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFactoryLaunchingPage.png"/></p>
Select the build-in function to copy data.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFactoryIngest.png"/></p>
From there, a wizard will help to navigate to choose the source and destination. For this project, the source is the SQL database and the destination is the storage previously created. In the end, a "pipeline" is created. 
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/SQLToBlobPipeline.png"/></p>
</br>

### Data Flow
Within the data factory, data can also be transformed. First a data source needs to be created, where a wizard will help guide through the process of defining the source. In this step, the source will be the previous file exported from the "pipeline".
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFlow.png"/></p>
By doing a right-click on the first flow, there are options to transform and manipulate the data.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFlowOptions.png"/></p>
For this flow, a filter will be used to filter the data from the database by the state of Alabama.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFlowOptionsFilterAdded.png"/></p>
Last but not list, a "Sink" for the destination needs to be added, and then the flow can be triggered.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFlowFinal.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFlowFinalScreen.png"/></p>
</br>




