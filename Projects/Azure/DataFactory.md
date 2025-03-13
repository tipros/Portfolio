# Azure Data Factory

In Azure, a pipeline was created with Data Factory to retrieve data from a SQL database, and export the data to a CSV file.
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

<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFactoryLaunchingPage.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/DataFactoryIngest.png"/></p>

</br>




