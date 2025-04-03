# Facial Recognition

There are two Azure AI services that you can use to build solutions that detect faces or people in images: Azure AI Vision and Face service.
</br>
</br>
The Azure AI Vision service enables you to detect people in an image, as well as returning a bounding box for its location.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/face-options.png"/></p>
The Face service provides comprehensive facial detection, analysis, and recognition capabilities.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/face-service.png"/></p>

Code to test the 2 services is cloned from the lab 4 from https://github.com/MicrosoftLearning/mslearn-ai-vision and Python is the preferred language for this exercise.

## Facial Recognition with Azure AI Vision Service
For the factial recognition, and exising AI service will be used. 
</br>
In the source code in path "\mslearn-ai-vision\Labfiles\04-face\Python\computer-vision", the .env file will be updated with the endpoint URL and API Key for the AI service.
The updated code for the file can be found at [here](https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/detect-people.py)
</br>
Run the code with this command>python detect-people.py
</br>
The following result will be shown in the terminal:
</br>
<blockquote>
Analyzing  images/people.jpg</br>
People in image:</br>
 {'x': 783, 'y': 320, 'w': 16, 'h': 189} (confidence: 0.29%)</br>
  Results saved in people.jpg
  </blockquote>
<p><img width="300" height="200" src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/people.jpg"/></p>

## Facial Recognition with Face Service
For the factial recognition, a Face Service resource needs to be created. A wizard will guide through the creation of the resource.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/facemarket.png"/></p>
In the source code in path "\mslearn-ai-vision\Labfiles\04-face\Python\face-api", the .env file will be updated with the endpoint URL and API Key for the AI service.
The updated code for the file can be found at [here](https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/analyze-faces.py)
</br>
Run the code with this command>python analyze-faces.py
</br>
The following result will be shown in the terminal:
</br>
<blockquote>
Detect faces</br>
Any other key to quit</br>
Enter a number:1</br>
Detecting faces in images\people.jpg</br>
2 faces detected.</br>
</br>
Face number 1</br>
 - Head Pose (Yaw): -8.1</br>
 - Head Pose (Pitch): -13.2</br>
 - Head Pose (Roll): -4.3</br>
 - Blur: BlurLevel.LOW</br>
 - Mask: MaskType.NO_MASK</br>
</br>
Face number 2</br>
 - Head Pose (Yaw): 3.3</br>
 - Head Pose (Pitch): -18.0</br>
 - Head Pose (Roll): -9.2</br>
 - Blur: BlurLevel.MEDIUM</br>
 - Mask: MaskType.NO_MASK</br>
</blockquote>
<p><img width="300" height="200" src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/detected_faces.jpg"/></p>
