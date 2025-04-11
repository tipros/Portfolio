# Question and Answering with Azure AI Language

Azure AI Language includes a question answering capability, 
to define a knowledge base of question and answer pairs 
that can be queried using natural language input. 
The knowledge base can be published to a REST endpoint 
and consumed by client applications such as bots.
</br></br>

The knowledge base can be created from existing sources, including:
Web sites containing frequently asked question (FAQ) documentation.
Files containing structured text, such as brochures or user guides.

## Create an Azure AI Language Service
Search Azure language from the Azure market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceMarket.png"/></p>
A wizard will guide through the creation of the resource. Select Custom Question Answwering 
and follow the next steps similarly to other Azure resources.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceOptions.png"/></p>

## Create Question Answer Pairs
Go to the Language Studio portal at https://language.cognitive.azure.com/ and sign in using the Microsoft account associated with your Azure subscription.
</br>

If prompted to choose a Language resource, select the following settings:
<pre>
- Azure Directory: The Azure directory containing your subscription.
- Azure subscription: Your Azure subscription.
- Resource type: Language
- Resource name: The Azure AI Language resource you created previously.
</pre>

<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortal.png"/></p>
Create a new project by selecting Custom Question Answwering 
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortalNewProject.png"/></p>
Select English as the default language and enter the following below for the project.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortalProjectOptions.png"/></p>
Create a new resource. 
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortalKB.png"/></p>
Provide the following information for the new resource:
<pre>
Name: Learn FAQ Page
URL: https://docs.microsoft.com/en-us/learn/support/faq
</pre>
Create a chit chat resource. This resource will be the default response if a question is
not recognized from the question and answer pair.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortalChitChat.png"/></p>
Deploy the knowledge base.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortalKBDeploy.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/LanguageServiceCognitivePortalKBDeployed.png"/></p>

## Call Language Service
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Text/ChatQandA.png"/></p>

