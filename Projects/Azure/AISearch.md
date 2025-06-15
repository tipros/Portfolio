# Using AI Search
In this project, AI Search will be used to index a set of documents from a fictional travel agency. 
The indexing process involves extracting key information to make them searchable, 
and generating a knowledge store containing data assets for additional analysis.

<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/ai-search.png"/></p>

## Create Resources
To complete this exercise, an AI Search service and storage account will be created from https://portal.azure.com

<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/ai-search-market.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-storage.png"/></p>

## Upload Documents
To documents to upload are at https://github.com/microsoftlearning/mslearn-ai-information-extraction/raw/main/Labfiles/knowledge/documents.zip
</br></br>
The documents are uploaded to the storage account, into a newly created container called <b>documents</b>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-storage-docsuploaded.png"/></p>
<b><i>Note:</i></b> For simplicity, set permission at the storage account level to anonymous so that the files can be accessed
by the indexing process

## Create the Index
To create an index, data will be imported to the AI Search service from the blog storage that has the documents.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/search-index.png"/></p>

During the import process in the section <b>Add enrichments</b>, Enable OCR and merge all text into merged_content field.
The following fields are selected for enrichment.
<pre>
Cognitive Skill         Field name
Text Cognitive          Skills	 	 
Extract people names    people
Extract location names  locations
Extract key phrases     keyphrases
  
Image Cognitive                 Skills	 	 
Generate tags from images       imageTags
Generate captions from images	imageCaption
</pre>

In the Save enrichments to a knowledge store section, select the following:
<pre>
Azure file projections: Image projections
Azure table projections: Documents, Key phrases
Azure blob projections: Document
</pre>

In the Customize target index, the following is selected.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-search-index-target.png"/></p>

After running the import once, the index and indexer are created.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-search-index.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-search-indexer.png"/></p>

After running an indexer that uses a skillset to create a knowledge store, the enriched data extracted by the indexing process
is persisted in the knowledge store projections.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/knowledge-store.png"/></p>

<b>Knowledge Store</b>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-storage-knowledge.png"/></p>
<b>Projection</b> JPEG files are created for each image that was extracted from the documents during the indexing process.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-storage-skills.png"/></p>
<b>Table</b>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Search/azure-storage-table.png"/></p>

## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/microsoftlearning/mslearn-ai-information-extraction from 
Azure Powershell and the code is under mslearn-ai-info/Labfiles/knowledge/python 
</br></br>

The endpoint URL and API key needs to be udpated inside the .env file directly. When executing the code from search-app.py, 
the results below with the corresponding prompts.

<pre>
Prompt Input: London

Search returned 2 documents:

Document: London Brochure.pdf
 - Locations:
   - London
   - city
   - England
   - United
   - River Thames
   - Great
   - Britain
   - Romans
   - Middlesex
   - Essex
   - Surrey
   - Kent
   - Hertfordshire
   - Greater London
   - London Hotels
   - Buckingham Hotel
   - hotel
   - Buckingham Palace
   - Regent’s Park
   - Trafalgar
   - The City Hotel
   - Tower Bridge
   - Tower of London
   - Kensington Hotel
   - Earl’s Court
   - Trafalgar Square
 - People:
   - Margie
 - Key phrases:
   - The Kensington Hotel Budget accommodation
   - 1.12-square- mile medieval boundaries
   - following accommodation options
   - The Buckingham Hotel
   - The City Hotel
   - Tower Bridge Fountains
   - Comfortable hotel
   - Buckingham Palace
   - United Kingdom
   - River Thames
   - major settlement
   - 19th century
   - Best time
   - Averag Precipitation
   - Average Temperature
   - major sights
   - Trafalgar Square
   - Luxury rooms
   - walking distance
   - populous city
   - Travel Presents
   - ancient core
   - Greater London
   - London Assembly
   - London Hotels
   - Margie
   - capital
   - England
   - south
   - island
   - Britain
   - two
   - millennia
   - Romans
   - metropolis
   - Middlesex
   - Essex
   - Surrey
   - Kent
   - Hertfordshire
   - Mayor
   - Leisure
   - Outdoors
   - Historical
   - Arts
   - Culture
   - Jun-Aug
   - Regent
   - Park
   - Earl
   - Court
   - trip

Document: Margies Travel Company Info.pdf
 - Locations:
   - Accommodation
   - Dubai
   - Las Vegas
   - London
   - New York
   - San Francisco
 - People:
   - Marjorie Long
   - Logan Reid
   - Emma Luffman
   - Deepak Nadar
 - Key phrases:
   - world-leading travel agency
   - best travel experts
   - international reach
   - Currency Exchange
   - Las Vegas
   - New York
   - San Francisco
   - leadership team
   - Marjorie Long
   - Logan Reid
   - Emma Luffman
   - Deepak Nadar
   - Strategic Director
   - Margie
   - local
   - expertise
   - Flights
   - Accommodation
   - Transfers
   - Visas
   - Excursions
   - trips
   - Dubai
   - London
   - CEO
   - CFO
   - website


Pomprt Input: flights
Search returned 1 documents:

Document: Margies Travel Company Info.pdf
 - Locations:
   - Accommodation
   - Dubai
   - Las Vegas
   - London
   - New York
   - San Francisco
 - People:
   - Marjorie Long
   - Logan Reid
   - Emma Luffman
   - Deepak Nadar
 - Key phrases:
   - world-leading travel agency
   - best travel experts
   - international reach
   - Currency Exchange
   - Las Vegas
   - New York
   - San Francisco
   - leadership team
   - Marjorie Long
   - Logan Reid
   - Emma Luffman
   - Deepak Nadar
   - Strategic Director
   - Margie
   - local
   - expertise
   - Flights
   - Accommodation
   - Transfers
   - Visas
   - Excursions
   - trips
   - Dubai
   - London
   - CEO
   - CFO
   - website
</pre>
