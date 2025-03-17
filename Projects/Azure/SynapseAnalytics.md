# Azure Synapse Analytics

Azure Data Factory is typically used for ETL. Azure Synapse Analystic on the other hand combines 
data integration (similar to ADF), data warehousing, and big data analytics. Synapse is designed for 
large-scale data processing and analysis, offering features like serverless and dedicated SQL pools, Spark integration, 
and machine learning capabilities

## Creating an Azure Synapse Resource
An Azure Synapse Resource is created from the market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/azuressynapsemarket.png"/></p>
A data lake resouce needs to be created. A wizard provides guidance to create the resources.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/azuresynapsedatalakefrom.png"/></p>

## Accessing the Azure Synapse Studio
Upon successful creation of the resources, the list of resources are listed in the resource group where everything is grouped. 
To access the Azure Synapse Resource, click on the workspace.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/azureresourcesforsynapse.png"/></p>
Click on Open Synapse Studio.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsestudioopen.png"/></p>

## Exploring Azure Synapse Studio
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsestudiohome.png"/></p>
On the left, click on the data (database icon).
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapseconnectsource.png"/></p>
From there, a connection can be used to connect to different types of sources. For this scenario, the menu Browse Gallery is selected.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsesourcesmaplegallery.png"/></p>
The NYC sample is selected and a preview of the data is displayed.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsesourcesmaplegallerynyc.png"/></p>
The sample data can be saved and will show in the list of linked data sets.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsesourcesmaplegallerynycds.png"/></p>
The data can be queried and filtered, and charts can be generated.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsesourcesmaplegallerynycgraph.png"/></p>
The data can be connected the Sparks pool, and then the data can be manipulated similarly to a Juypter Notebook.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsesourcesmaplegallerynycnotebook.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/synapsesourcesmaplegallerynycnotebookshowframe.png"/></p>





