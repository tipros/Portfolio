# Develop a Multi-Agent Solution

In this project, two AI agents using the Semantic Kernel SDK will be deployed to demonstrate the orchestration between the two agents: an Incident Manager agent and a DevOps agent.
The Incidedent Manager reviews the log files and recommends a solution. The DevOps agent will receive the solution and call the function to perform the resolution.
 </br>

## Create Resources
To complete this exercise,a gpt-4o model will be created from https://ai.azure.com
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-seachmodel.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-usethismodel.png"/></p>


## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-agents
and the code is in the folder ai-agents/Labfiles/05-agent-orchestration/Python. The code is executed in Azure through the CLI and requires authentication in PowerShell with the command: az login 
</br></br>
In addition, the Semantic Kernel SDK will need to be installed: pip install python-dotenv azure-identity semantic-kernel[azure]
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/agent_chat.py
</br></br>
With Python projects, the .env file has to be updated with the project endpoint.
</br>
When executing the Python code, below will be displayed at the prompt. The code reads existing log files.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-multi-prompt.png"/></p>
