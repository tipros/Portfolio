# Creating and Consuming an AI Service

In this exercise, the following will be accomplished:
<ol>
  <li>Create an Azure AI Service</li>
  <li>Use a REST API and SDK to consume an Azure AI service.</li>
</ol>

## Creating an AI Service
In the Azure Portal, create an AI Service multiservice account.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/AIServiceCreate.png"/></p>
Upon successful creation, the service is listed in the resource group it was associated with.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/AIResources.png"/></p>
Under Resource Management, the keys and endpoints are listed and will later be used to the REST API and SDK to leverage.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/AIServiceEndPoint.png"/></p>

## Consume AI Service via a REST API and SDK
From VS Code, the code below will be cloned from https://github.com/MicrosoftLearning/mslearn-ai-services
</br> 
The source provides examples for both C# and Python. For this exercise, Python will be used.
</br>
The .env file for the REST API is updated withe URL and key from the AI service previously created.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/ClientEnv.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/RunTerminalFromFolder.png"/></p>
The REST API code is executed below.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/RunTerminalClientCode.png"/></p>
The SDK .env file is updated withe URL and key from the AI service previously created.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/SDKEnv.png"/></p>
Prerequisites installed for the SDK to run correcly.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/RunTerminalSDKPrerequisites.png"/></p>
The SDK code is executed below.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/RunTerminalSDKCode.png"/></p>
