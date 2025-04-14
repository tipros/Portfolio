# Conversational Language Understanding Model

In the conversationa language understanding model, the design pattern is as follow:
<ol>
<li>An app accepts natural language input from a user.</li>
<li>A language model is used to determine semantic meaning (the user's intent).</li>
<li>The app performs an appropriate action.</li>
</ol>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/language-understanding-app.png"/></p>

A natural language understanding app is created using Azure AI Language. The following steps were taken.
<ol>
  <li>Provision an Azure AI Language resource.</li>
  <li>Use patterns to differentiate similar utterances.</li>
  <li>Train, test, publish, and review a model.</li>
</ol>

## Azure AI Language Resource
For this project, an existing Azure AI Language resource will be used.
</br>
Go to the Language Studio portal at https://language.cognitive.azure.com/ and sign in using the Microsoft account associated with the Azure subscription.
</br>

If prompted to choose a Language resource, select the following settings:
<pre>
- Azure Directory: The Azure directory containing your subscription.
- Azure subscription: Your Azure subscription.
- Resource type: Language
- Resource name: The Azure AI Language resource you created previously.
</pre>

A new project of type <b>Conversational language understanding</b> is created and named <b>Clock</b>.

## Create Intent
In the newly created project, intents are created. The following intents are created with corresponding utterances: GetTime, GetDay, and GetDate.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/langauge-label-itentlist.png"/></p>
Intents can be created from a list or using a prebuilt intents such as a date. Intents can be associated to entities as well.

## Train and Test
Once the intents and utterances are established, the model needs to be trained. 
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/language-train.png"/></p>
After the model has been trained, it can be then tested and deployed.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/language-trained.png"/></p>

## Testing with Code
To test the code, the GitHub code was cloned from https://github.com/MicrosoftLearning/mslearn-ai-language 
</br>
The folder Labfiles/03-language contains the code to test the Clock project, and Python will be used. 
Hence, the .env file has to be updated with the endpoint URL and API key of Azure Language Service.
</br>
The updated Python code to call the Clock project is at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/clock-client.py
</br>
When running the code, the output will look similar to below:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/vscode-clock-console-01.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/vscode-clock-console-02.png"/></p>
