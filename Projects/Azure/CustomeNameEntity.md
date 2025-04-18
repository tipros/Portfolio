# Custom Named Entity Recognition 

Custom named entity recognition (NER), also known as custom entity extraction, 
is one of the many features for natural language processing (NLP) offered by Azure AI Language service.
Custom NER enables developers to extract predefined entities from text documents.

</br>
To accomplish this in Azure, the following steps will be taken:
<ol>
  <li>Deploy an AI language service for custom classification</li>
   <li>Build a custom text classification project.</li>
   <li>Tag data, train, and deploy a model.</li>
   <li>Submit classification tasks from an application.</li>
</ol>

## Create an Azure AI Language Service
Search Azure language from the Azure market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceMarket.png"/></p>
A wizard will guide through the creation of the resource. Select Custom Text Classification
and follow the next steps similarly to other Azure resources. While creating the language service, 
a storage account is required to be associated with the service.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/languageservicecustom.png"/></p>
The text file to upload for training are located at https://aka.ms/entity-extraction-ads and will need
to be uploaded to the storage account.  A container called "classifieds" will need to be created in the storage account
and Blob anonymous read access will be enabled. 

## Build Custom Text Classification Project
Go to the Language Studio portal at https://language.cognitive.azure.com/ and sign in using the Microsoft account associated with your Azure subscription.
</br>

If prompted to choose a Language resource, select the following settings:
<pre>
- Azure Directory: The Azure directory containing your subscription.
- Azure subscription: Your Azure subscription.
- Resource type: Language
- Resource name: The Azure AI Language resource you created previously.
</pre>

Create a new project for <b>Custom named entity recognition</b>. 
</br>
The Connect storage page appears. All values will already have been filled. 
</br>
On the Enter basic information pane, set the following:
<pre>
Name: CustomEntityLab
Text primary language: English (US)
Description: Custom entities in classified ads
</pre>
In the labeling section, the list of files from the storage account are displayed. 
Three types of entities are created, which will be used to label in the text files.
Labels are added by identifying the entities inside the text filesaccordingly.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageLabels.png"/></p>
When the labeling is completed, the model is then trained, deployed, and tested.

## Call Language Service
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-language 
and the code is in the folder Labfiles/05-custom-entity-recognition
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/custom-entities.py
</br></br>
With Python projects, the .env file has to be updated with endpoint URL and API key created in the Azure portal. 
The project name will is obtained from the Language Studio portal.
</br>
When executing the Python code, below is the sample output (the code reads a directory of files and provided a confidence score).
<pre>
test1.txt
        Entity 'Bluetooth earbuds' has category 'ItemForSale' with confidence score of '0.81'
        Entity '$100' has category 'Price' with confidence score of '0.85'
        Entity 'Sacramento, CA' has category 'Location' with confidence score of '0.89'
test2.txt
        Entity 'Dog harness' has category 'ItemForSale' with confidence score of '0.92'
        Entity '$20' has category 'Price' with confidence score of '0.88'
        Entity 'Tucson, AZ' has category 'Location' with confidence score of '0.89'
</pre>
