# Text Analysis with OCR

Azure AI provides two different features that read text from documents and images:</br>
- Image Analysis Optical character recognition (OCR)</br>
- Document Intelligence</br>

Image Analysis Optical character recognition (OCR):
- Use this feature for general, unstructured documents with smaller amount of text, or images that contain text.</br>
- Results are returned immediately (synchronous) from a single API call.</br>
- Has functionality for analyzing images past extracting text, including object detection, describing or categorizing an image, generating smart-cropped thumbnails and more.</br>
- Examples include: street signs, handwritten notes, and store signs.</br>

</br>
In this exercise, OCR will be used for text recognition by using the Python code from Git Hub at https://github.com/MicrosoftLearning/mslearn-ai-services located in the folder Labfiles\05-ocr
</br></br>
The updated Python file is at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/read-text.py
</br></br>
The .env file needs to updated with the endpoint URL and API key of the AI service that will be used.
</br></br>
The following images will be analyzed for text with OCR.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/Lincoln.jpg"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/Note.jpg"/></p>
Below the terminal results of running the Python code:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/OCR-Results-01.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/OCR-Results-02.png"/></p>
Below are the text detected in the images:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/text01.jpg"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/text02.jpg"/></p>
