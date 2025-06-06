# Deploy an AI Agent

In this project, an Azure AI Agent Service will be used to create a simple agent that analyzes data and creates charts. 
The agent uses the built-in Code Interpreter tool to dynamically generate the code needed to create charts as images, then saving the created image.
 </br>

## Create Resources
To complete this exercise, a new project and agent will be created from https://ai.azure.com
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/ai-foundry-home.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/ai-foundry-agents-playground.png"/></p>
The model deployed will be the GPT-4o base model.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/ai-foundry_deploye_gpt4o.png"/></p>

## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-agents
and the code is in the folder ai-agents/Labfiles/02-build-ai-agent/Python. The code is executed in Azure through the CLI.
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/agent.py
</br></br>
With Python projects, the .env file has to be updated with the project endpoint.
</br>
When executing the Python code, and a question is answered at the prompt, the results are below where the agent responds and generates a chart.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-prompt.png"/></p>
