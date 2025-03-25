# Analyze Images with Azure AI Vision

Azure AI Vision is an AI capability to interpret visual input by analyzing images. 
Common computer vision tasks, including analysis of images to suggest captions and tags, detection of common objects and people.

## Image Analysis of Image
The source for the image analysis was cloned from https://github.com/MicrosoftLearning/mslearn-ai-vision
</br>
Python is used to code, and the Endpoint URL and API Key are updated in the .env file.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/vscodevisionkeys-01.png"/></p>

The updated Python file with all the necessary changes code is [here.](https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/image-analysis.py)
</br>
Image file to analyze:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/street.jpg"/></p>
Running the code, command>python image-analysis.py images/street.jpg
</br></br>
<blockquote>
Results of the code executed:</br>
Analyzing image...</br>

Caption:</br>
 Caption: 'a man walking a dog on a leash on a street' (confidence: 82.05%)</br></br>

Dense Captions:</br>
 Caption: 'a man walking a dog on a leash on a street' (confidence: 82.05%)</br>
 Caption: 'a man walking on a street' (confidence: 69.03%)</br>
 Caption: 'a yellow car on the street' (confidence: 78.17%)</br>
 Caption: 'a black dog walking on the street' (confidence: 75.33%)</br>
 Caption: 'a blurry image of a blue car' (confidence: 82.01%)</br>
 Caption: 'a yellow taxi cab on the street' (confidence: 72.42%)</br></br>

Tags:</br>
 Tag: 'outdoor' (confidence: 99.87%)</br>
 Tag: 'land vehicle' (confidence: 99.02%)</br>
 Tag: 'vehicle' (confidence: 98.89%)</br>
 Tag: 'building' (confidence: 98.55%)</br>
 Tag: 'road' (confidence: 95.98%)</br>
 Tag: 'wheel' (confidence: 95.14%)</br>
 Tag: 'street' (confidence: 94.71%)</br>
 Tag: 'person' (confidence: 93.01%)</br>
 Tag: 'clothing' (confidence: 91.19%)</br>
 Tag: 'taxi' (confidence: 90.95%)</br>
 Tag: 'car' (confidence: 84.01%)</br>
 Tag: 'dog' (confidence: 82.68%)</br>
 Tag: 'yellow' (confidence: 77.08%)</br>
 Tag: 'walking' (confidence: 74.11%)</br>
 Tag: 'city' (confidence: 64.80%)</br>
 Tag: 'woman' (confidence: 57.53%)</br></br>

Objects in image:</br>
 car (confidence: 72.40%)</br>
 taxi (confidence: 77.00%)</br>
 person (confidence: 78.10%)</br>
 dog (confidence: 54.40%)</br>
  Results saved in objects.jpg
</blockquote>
</br>
Objects identified in image:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/objects.jpg"/></p>
