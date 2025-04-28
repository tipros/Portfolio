# Azure Speech Translator

The Azure AI Speech translator provides an API for translating speech to text.
</br></br>
The translator can translate from one language to another, one language to many, or 
translate to provide a phonetic translation (transliteration).
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Speech/translate-speech-small.png"/></p>

## Create an Azure Translator Service
Search Translator from the Azure market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/translator-marketplace-service.png"/></p>
A wizard will guide through the creation of the resource.

## Call Speech Translator Service
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-language 
and the code is in the folder Labfiles/08-speech-translation
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/translator.py
</br></br>
With Python projects, the .env file has to be updated with <b>region</b> and API key created in the Azure portal. 
</br>
When executing the Python code, below is the sample output (input is language code, then speech).
<pre>
Enter a target language
 fr = French
 es = Spanish
 hi = Hindi
 Enter anything else to stop
fr
Speak now...
Translating "Hello, I'm hungry."
Bonjour, j’ai faim.

Enter a target language
 fr = French
 es = Spanish
 hi = Hindi
 Enter anything else to stop
es
Speak now...
Translating "How are you?"
¿Cómo estás?

Enter a target language
 fr = French
 es = Spanish
 hi = Hindi
 Enter anything else to stop

</pre>
