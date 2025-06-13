# Using Prebuilt Models to Analyze Documents
In this project, a prebuilt model is selected to analyze documents with AI intelligence documents.
</br></br>
Example of prebuilt models with AI intelligence document trained on specific form types:
<pre>
- Invoice model
- Receipt model
- US Tax model
- ID document model
- Business card model
- Health insurance card model
- Marriage certificate
- Credit/Debit card model
- Mortgage documents
- Bank statement model
- Pay Stub model
- Check model
</pre>

Other models are designed to extract values from less structured documents:
<pre>
- Read model: Extracts text and languages from documents.
- General document model: Extract text, keys, values, entities, and selection marks from documents.
- Layout model: Extracts text and structure information from documents.
</pre>

Features and analysis capabilities of prebuilt models
<pre>
- Text extraction
- Key-value pairs
- Entities
- Selection marks
- Tables
- Fields
</pre>

Input file requirements:
<pre>
- The file must be in JPEG, PNG, BMP, TIFF, or PDF format (read model can accept Microsoft Office files)
- The file must be smaller than 500 MB for the standard tier, and 4 MB for the free tier.
- Images must have dimensions between 50 x 50 pixels and 10,000 x 10,000 pixels.
- PDF documents must have dimensions less than 17 x 17 inches or A3 paper size.
- PDF documents must not be protected with a password
</pre>

Types of entities detected:
<pre>
- Person. The name of a person.
- PersonType. A job title or role.
- Location. Buildings, geographical features, geopolitical entities.
- Organization. Companies, government bodies, sports clubs, musical bands, and other groups.
- Event. Social gatherings, historical events, anniversaries.
- Product. Objects bought and sold.
- Skill. A capability belonging to a person.
- Address. Mailing address for a physical location.
- Phone number. Dialing codes and numbers for mobile phones and landlines.
- Email. Email addresses.
- URL. Webpage addresses.
- IP Address. Network addresses for computer hardware.
- DateTime. Calendar dates and times of day.
</pre>

## Create Resources
To complete this exercise, a new resource Document Intelligence is required to be created from https://portal.azure.com

## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-ai-document-intelligence from VS Code
and the code is in the folder Labfiles/01-prebuild-models/Python. 
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/document-analysis.py
</br>
The endpoint URL and API key needs to be udpated inside the file directly. The following document is analyzed.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/sample-invoice.png"/></p>
When executing the Python code, the analysis for the document is as follow:
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Agent/extrated-analysis-results.png"/></p>
