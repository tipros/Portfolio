# AI Custom Vision

Azure AI Custom Vision service enables you to build your own computer vision models for image classification or object detection.

<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/image-classification.png"/></p>

To use the Azure AI Custom Vision service, two kinds of Azure resources are required.
</br>
</br>
A <b>training</b> resource used to train your models:
<ol>
<ul>An Azure AI services multi-service resource.</ul>
<ul>An Azure AI Custom Vision (Training) resource.</ul>
</ol>
A <b>prediction</b> resource, used by client applications to get predictions from your model:
<ol>
<ul>An Azure AI services multi-service resource.</ul>
<ul>An Azure AI Custom Vision (Prediction) resource.</ul>
</ol>
</br>

Code for this exercise were cloned from this GitHub repository: https://github.com/MicrosoftLearning/mslearn-ai-vision

## Create a Custom Vision Resource
Search for Custom Vision in the market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionmarket.png"/></p>
A wizard will guide through the creation of the custom vision resource. Make sure to select <b>Both</b> for the Create options.

## Custom Vision Portal
Visit the Vision Portal at https://customvision.ai
</br>
Create a new project.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionhome.png"/></p>
Fill in the form as shown below.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionprojectform.png"/></p>
Upload data from LabFiles/07-custom-vision-image-classification/training-images/ and tag according to the fruit type.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionprojectworkspace.png"/></p>
Apple data.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisiondataapples.jpg"/></p>
Banana data.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisiondatabanana.png"/></p>
Orange data.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisiondataorange.png"/></p>
All images loaded and tagged.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisiondataloaded.jpg"/></p>
Click Train to train a classification model using the tagged images. Select the Quick Training option.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionprojecttrain.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionprojecttraining.png"/></p>
Upon completion, the portal will show the results as shown below.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/customvisionprojecttrainingdone.png"/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
<p><img src=""/></p>
