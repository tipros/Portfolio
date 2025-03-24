# Implement Azure AI Content Safety

Azure AI allows the implementation of content safety that helps filter out content that is provided to Azure AI:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/four-perspectives.jpg"/></p>
In this exercise, a content safety resource will be created, and applied to a prompt.

## Create Content Safety
Search for the content safety in the Azure market place for resources, and create the new resource by following the wizard.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/contentsafetymarket.png"/></p>
Take note of the API key and endpoint URL for future reference.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/contentsafetyendpoint.png"/></p>

## Use Content Safety in Azure AI Foundry
From the Azure Foundy page, go to Content Safey and select Prompt Shields, then select Try it out.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/contentsafetypromptshield.png"/></p>
Select Use Prompt Attack Content, and click on Run Test.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/contentsafetyprompttest.png"/></p>
The results are as follow:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/contentsafetypromptresults.png"/></p>

## Use Content Safety with Code
With the last test run in Azure AI Foundy, code is provided in C# or Python. The Python code is copied and can be found 
[here.](https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/prompt-shield.py)
</br>
In VS Code, update the settings below with API Key and URL endpoint for the Azure AI Content Safety resource. In the addition, the prompt needs to be updated in the code as well.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/vscodecontentsafety.png"/></p>
When the code is executed, the results should similar to below:
</br>
Response status code: 200</br>
Response content: {"userPromptAnalysis":{"attackDetected":true},"documentsAnalysis":[]}</br>
shieldPrompt result: {'userPromptAnalysis': {'attackDetected': True}, 'documentsAnalysis': []}</br>


