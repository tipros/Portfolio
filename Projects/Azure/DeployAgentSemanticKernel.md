# Deploy an AI Agent with Semantic Kernel SDK

In this project, an Azure AI Agent Service and Semantic Kernel SDK will be used to create an AI agent that processes expense claims.
 </br>

## Create Resources
To complete this exercise,a gpt-4o model will be created from https://ai.azure.com
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-seachmodel.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-usethismodel.png"/></p>


## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-agents
and the code is in the folder ai-agents/Labfiles/04-semantic-kernel/python. The code is executed in Azure through the CLI and requires authentication in PowerShell with the command: az login 
</br></br>
In addition, the Semantic Kernel SDK will need to be installed: pip install python-dotenv azure-identity semantic-kernel[azure]
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/semantic-kernel.py
</br></br>
With Python projects, the .env file has to be updated with the project endpoint.
</br>
When executing the Python code, and a question is answered at the prompt, the results are below.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-prompt.png"/></p>
