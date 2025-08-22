# Build a Semantic Kernel object

In this project, an Azure OpenAI resource is created and deployed to the Semantic Kernel.
The Semantic Kernel connects to the endpoint and allow prompts to the large language model (LLM) directly from code.
 </br>

## Create Resources
To complete this exercise,a gpt-4o model will be created from https://ai.azure.com
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-seachmodel.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-usethismodel.png"/></p>


## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-semantic-kernel
and the code is in the folder 01-build-your-kernel/Python.
</br></br>
In addition, the Semantic Kernel SDK will need to be installed: pip install python-dotenv azure-identity semantic-kernel[azure]
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/kernel.py
</br></br>
With Python projects, the .env file has to be updated with the project endpoint.
</br>
When executing the Python code, the program returns a list of 10 breakfast foods with eggs and cheese.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Kernel/01-vscode-output.png"/></p>
