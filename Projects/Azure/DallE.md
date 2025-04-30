# Generate Images with AI

In this project, the OpenAI DALL-E generative AI model is used to generate images. A client application is developed 
by using Azure AI Foundry and the Azure OpenAI service to generate the image based on the prompt provided.

## Create Project
From https://ai.azure.com, a new project is created. A wizard will guide through the creation of the new project and hub.
</br>
Deploy a new model and select Dall-E. When testing in the playground, and entering the following prompt, the image is generated below> Create an image of a robot eating pizza
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/dalleimagegenerated.png"/></p>

## Call Speech Translator Service
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-vision 
and the code is in the folder Labfiles/09-dalle-client
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/dalle-client.py
</br></br>
With Python projects, the .env file has to be updated with the HUB connection string and name of deployment.
</br>
When executing the Python code, the image below is generated when prompted with>Create an image of a robot eating pizza
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/dall-e-3-sdk.png"/></p>
