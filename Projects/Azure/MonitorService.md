# Creating Alerts and Monitoring Dashboard for Azure AI Service

In Azure, it is possible to monitor the activities of various resources, including AI services.
</br></br>
In this exercise, the following will be accomplished:
<ol>
  <li>Create alerts Azure AI services.</li>
  <li>View metrics for Azure AI services.</li>
</ol>

To trigger alerts and metrics, a lab will retrieved from this Git Hub repository: https://github.com/MicrosoftLearning/mslearn-ai-services
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/vscodelab3.png"/></p>

## Create an Alert
Alerts can be created for a given resouce by going to the menu Monitoring > Alert</br>
Click on Create alert rule.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alerthome.png"/></p>
Select See All Signals.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alertcreaterule.png"/></p>
Select List Keys.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alertsetrule.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alertruleselected.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alerterulefinalform.png"/></p>
The alert is created, but empty for now.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alertemptydb.png"/></p>
Run the following command to trigger the alerts. This will retrieve the keys of the AI service.</br>
command>az cognitiveservices account keys list --name "resourceName" --resource-group "resourceGroup"</br>
</br>
The alerts are generated on the dashboard.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alertdb.png"/></p>
Click on the details of the alert to get more information.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/alertdetail.png"/></p>

# Create Metrics Dashboard
To create a metric dashboard, select Monitoring and Metrics, then create a new chart.The metric to visualize will be Total Calls,
and in the Aggregation list, Count is selected.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/metricdb.png"/></p>
In VS Code for the lab for this exercise, the endpoint URL and keys are updated, then the cmd file is executed to trigger the metrics.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/VSCodeLab3TestCmd.png"/></p>
After a few mins, the metrics can be visualized in the previously created metric.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/metricdbdata.png"/></p>

