# Create Semantic Kernel Plugins

In this exercise, the Semantic Kernel is used to create an AI assistant that can search for and book flights for a user. 
A custom plugin functions is created to help accomplish the task.
 </br>

## Create Resources
To complete this exercise,a gpt-4o model will be created from https://ai.azure.com
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-seachmodel.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/agent-semkernel-usethismodel.png"/></p>


## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-semantic-kernel
and the code is in the folder /Labfiles/03-create-plugins/Python/
</br></br>
In addition, the Semantic Kernel SDK will need to be installed: pip install python-dotenv azure-identity semantic-kernel[azure]
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/plugins.py
</br></br>
With Python projects, the .env file has to be updated with the project endpoint.
</br>
When executing the initial Python code, the program reads a JSON file with a list of flights available for booking.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Kernel/03-vscode-outputa.png"/></p>
After configuring the kernel so that only selected functions are available to assist in providing travel information, 
the assistant is unable to book flights.
</br></br>

Updated code for the plug-in:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Kernel/03-vscode-filterplugin.png"/></p>
Output:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Kernel/03-vscode-outputb.png"/></p>
