# Azure Translator

The Azure AI Translator provides an API for translating text between 90 supported languages.
</br></br>
The translator can translate from one language to another, one language to many, or 
translate to provide a phonetic translation (transliteration).
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/translator-resource.png"/></p>

## Create an Azure Translator Service
Search Translator from the Azure market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/translator-marketplace-service.png"/></p>
A wizard will guide through the creation of the resource.

## Call Translator Service
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-language 
and the code is in the folder Labfiles/06b-translator-sdk
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/translate.py
</br></br>
With Python projects, the .env file has to be updated with <b>region</b> and API key created in the Azure portal. 
</br>
When executing the Python code, below is the sample output.
<pre>
137 languages supported.
(See https://learn.microsoft.com/azure/ai-services/translator/language-support#translation)
Enter a target language code for translation (for example, 'en'):
fr
Enter text to translate ('quit' to exit):Good morning America
'Good morning America' was translated from en to fr as 'Bonjour l’Amérique'.
Enter text to translate ('quit' to exit):quit
</pre>
