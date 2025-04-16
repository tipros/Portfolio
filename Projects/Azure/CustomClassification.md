# Custom Classification of Text

Azure AI Language service allows to classify text into custom groups. 
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
The text file to upload for training are located at https://aka.ms/classification-articles and will need
to be uploaded to the storage account.  A container called "articles" will need to be created in the storage account
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

Create a new project for <b>Custom text classification</b>. The project type is <b>Single label classification</b>.
</br>
The Connect storage page appears. All values will already have been filled. 
</br>
On the Enter basic information pane, set the following:
<pre>
Name: ClassifyLab
Text primary language: English (US)
Description: Custom text lab
</pre>
In the labeling section, the listt of files from the storage account are displayed.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/labeldata.png"/></p>
Labels are added, and then each article is labeled accordingly.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/labeldataclassified.png"/></p>
When the labeling is completed, the model is then trained, deployed, and tested.

## Call Language Service
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-language 
and the code is in the folder Labfiles/04-text-classification
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/classify-text.py
</br></br>
With Python projects, the .env file has to be updated with endpoint URL and API key created in the Azure portal. 
The project name will is obtained from the Language Studio portal.
</br>
When executing the Python code, below is the sample output (the code reads a directory of files and provided a confidence score).
<pre>
test1.txt was classified as 'Entertainment' with confidence score 0.3.
test2.txt was classified as 'Sports' with confidence score 0.34.
</pre>
