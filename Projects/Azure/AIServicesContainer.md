# Use an Azure AI Services Container

In this exercise, an AI service will be called from an container. An existing AI service will be used, and the Git Hub code used to call the service is lab 4 from the repository: 
https://github.com/MicrosoftLearning/mslearn-ai-services

# Create Container
Search Container Instances in the market place to create a new container.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/containerinstancemarket.png"/></p>
A wizard will guide through the creation of the container. Below are the options to select:
<ol>
<li>Subscription: Your Azure subscription</li>
<li>Resource group: Choose the resource group containing your Azure AI services resource</li>
<li>Container name: Enter a unique name</li>
<li>Region: Choose any available region</li>
<li>Availability zones: None</li>
<li>SKU: Standard
<li><b>Image source: Other Registry</b></li>
<li>Image type: Public</li>
<li><b>Image: mcr.microsoft.com/azure-cognitive-services/textanalytics/sentiment:latest</b></li>
<li>OS type: Linux</li>
<li>Size: 1 vcpu, 8 GB memory</li>
</ol>
</br>
For the network options, set to public, provide a unique name, and change the port from 80 to 5000.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/containernetwork.png"/></p>
For variables, the API Key, Billing, and Eula setting need to be set as shown below. The API KEY is one of the keys of the AI Services resource, 
and Billing is the URL of the endpoint of the AI Services resource.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/containervariables.png"/></p>
</br>
It takes 5-10 minutes to deploy the container. Once the container is in the status "Running", in the overview of the container are
IP address and FDQN of the container. Either the IP address or FDQN can be copied to a web browser with the port 5000, and the following page will be shown.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/container.png"/></p>
<p><img src=""/></p>

# Calling an AI Service from a Container
From VS Code in Lab 4, update the URL with that of the container with either the IP address or FDQN.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/VSCodeLab4TestCmd.png"/></p>
Execute the command> ./rest-test.cmd
</br>
The result will be a JSON reponse similar to below, provide a sentiment score from the input provided.
</br>
{"documents":[{"id":"1","sentiment":"positive","confidenceScores":{"positive":0.99,"neutral":0.0,"negative":0.0},
"sentences":[{"sentiment":"positive","confidenceScores":{"positive":0.99,"neutral":0.0,"negative":0.0},"offset":0,"length":29,"text":"The performance was amazing! "},
{"sentiment":"neutral","confidenceScores":{"positive":0.19,"neutral":0.47,"negative":0.34},"offset":29,"length":34,"text":"The sound could have been clearer."}],"warnings":[]},
{"id":"2","sentiment":"negative","confidenceScores":{"positive":0.0,"neutral":0.01,"negative":0.98},"sentences":[{"sentiment":"negative","confidenceScores":{"positive":0.0,"neutral":0.01,"negative":0.99},
"offset":0,"length":40,"text":"The food and service were unacceptable. "},{"sentiment":"negative","confidenceScores":{"positive":0.0,"neutral":0.02,"negative":0.98},"offset":40,"length":63,
"text":"While the host was nice, the waiter was rude and food was cold."}],"warnings":[]}],"errors":[],"modelVersion":"2022-11-01"}
