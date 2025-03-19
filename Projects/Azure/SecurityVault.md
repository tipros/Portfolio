## Using AI Services with Security and Vault

Access to Azure AI services is controlled through authentication keys, which are generated when an Azure AI services resource is created.
<p><img height="400" widht="400" src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/azure-key-vault.png"/></p>

From VS Code, the code below will be cloned from https://github.com/MicrosoftLearning/mslearn-ai-services
</br>The code has both C# and Python code. Python will be used.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/vscodelab2.png"/></p>

From an existing AI resource, replace the end-point and key from the file below:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/vscodecurl.png"/></p>
Execute the code>./rest-test.cmd
</br>
The results are below, where the language detected was English with a confidence score.
{"kind":"LanguageDetectionResults","results":{"documents":[{"id":"1","warnings":[],"detectedLanguage":{"name":"English","iso6391Name":"en","confidenceScore":1.0}}],"errors":[],"modelVersion":"2024-11-01"}}

## Create a Vault Resource
Create a vault resource by searching from the Azure portal. A wizard will guide through the process of creating the resource.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/keyvaultmarketplace.png"/></p>
Make sure to update the configuration settings, and enable Vault access policy.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/vaultconfigurationsettingspolicy.png"/></p>
Create a secret with one of the keys from the Azure service endpoints.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/valuecreatesecret.png"/></p>

## Create a Service Principal
A principal refers to an identity that can be authenticated and authorized to access Azure resources. A service principal is a security identity used by applications 
or services to access specific Azure resources. It's like a "user identity" or "service account" for an application.
</br></br>
To create a service principale, use the following command> az ad sp create-for-rbac -n "api://spName" --role owner --scopes subscriptions/"subscriptionId"/resourceGroups/"resourceGroup"
</br>
spName is the name given to your app. The subscription ID is the ID listed for the vault resource. The resource group is the group where the AI service resides in.
</br></br>
The results would look like something below (<i>save the information for future steps</i>):
</br>
{</br>
    "appId": "abcd12345efghi67890jklmn",</br>
    "displayName": "api://ai-app-",</br>
    "password": "1a2b3c4d5e6f7g8h9i0j",</br>
    "tenant": "1234abcd5678fghi90jklm"</br>
}</br>
</br>
Next, the principal ID needs to be retrieved with this command>az ad sp show --id <appId>
<br>
The "objectId" to save from the JSON results is "id".
</br></br>
To assign permission for your new service principal to access secrets in the Key Vault, run the following command, replacing "keyVaultName"
with the name of the Azure Key Vault resource and "objectId" with the value of the service principal's ID value that was saved.
</br>
command>az keyvault set-policy -n "keyVaultName" --object-id "objectId" --secret-permissions get list
</br></br>
Now the service principal identity will be used in an application, and the values of the .env file will be updated with all the values previously retrieved and saved.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/vscodeenvvault.png"/></p>
Run the python code with this command>python keyvault-client.py
</br>
The results is below when "Gracias" is entered at the prompt.
</br></br>
<i>
Enter some text ("quit" to stop)
Gracias</br>
Language: Spanish</br>
</br>
Enter some text ("quit" to stop)</br>
quit</br>
</i>
