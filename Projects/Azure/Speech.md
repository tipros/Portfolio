# Azure Speech

Azure AI Speech provides APIs that you can use to build speech-enabled applications. This includes:
<pre>
Speech to text
Text to speech
Speech Translation
Speaker Recognition
Intent Recognition
</pre>
This project will focus on the first capabilities: speect to text and text to speech.
</br></br>
Speech to text flow.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Speech/speech-to-text.png"/></p>
Text to speech flow.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Speech/text-to-speech.png"/></p>

## Create an Azure Speech Service
Search Speech from the Azure market place.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Speech/speech-resource.png"/></p>
A wizard will guide through the creation of the resource.

## Call Speech Service
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-language 
and the code is in the folder Labfiles/07-speech
</br></br>
The code for this project accomplishes the following:
<pre>
Use the Speech to text API to implement speech recognition
Use the Text to speech API to implement speech synthesis
Configure audio format and voices
Use Speech Synthesis Markup Language (SSML)
</pre>
</br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/speaking-clock.py
</br></br>
With Python projects, the .env file has to be updated with <b>region</b> and API key created in the Azure portal. 
</br>
When executing the Python code, below is the sample output. 
</br></br>
As input, the phrase "What is it?" is spoken then
transcribed to text. The response is then provided in the console, and via speech in a specified tone, and 
another via a Speech Synthesis Markup Language (SSML) input in another tone.
<pre>
Ready to use speech service in: eastus
Speak now...
What time is it?
The time is 16:44
</pre>
