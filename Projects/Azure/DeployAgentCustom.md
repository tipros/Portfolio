# Deploy an AI Agent using Custom Functions

In this project, an agent that can use custom functions as a tool to complete tasks is created.
A simple technical support agent is created that helps collect details of a technical problem and generate a support ticket.

<p>
To use an AzureAIAgent:
 <pre>
- Create an Azure AI Foundry project.
- Add the project connection string to Semantic Kernel application code (.env file for Python projects).
- Create an AzureAIAgentSettings object.
- Create an AzureAIAgent client.
- Create an agent definition on the agent service provided by the client.
- Create an agent based on the definition.
</pre>
</p>

<p>
To use plugins with AzureAIAgent:
<pre>
- Define plugin 
- Add the plugin to agent
- Invoke the plugin's functions
</pre>
</p>

## Create Resources
To complete this exercise, a new project and agent will be created from https://ai.azure.com
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/ai-foundry-home.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/ai-foundry-agents-playground.png"/></p>
The model deployed will be the GPT-4o base model.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/ai-foundry_deploye_gpt4o.png"/></p>

## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-agents
and the code is in the folder ai-agents/Labfiles/03-ai-agent-functions/Python. The code is executed in Azure through the CLI and requires authentication in PowerShell with command: az login 
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/agent-custom.py and https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/user_functions.py
</br></br>
With Python projects, the .env file has to be updated with the project endpoint.
</br>
When executing the Python code, and a question is answered at the prompt, the results are below where the agent responds and generates a ticket.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-custom-prompt.png"/></p>
