# Implement Retrieval Augmented Generation (RAG) with Azure OpenAI Service

 In this project, Azure AI Search will be used to index one's own data and use it with Azure OpenAI to augment prompts.
 </br>

Azure OpenAI enables developers to implement Retrieval Augmented Generation (RAG) by connecting supporting AI chat models to their own data. 
Those models can reference specific sources of data to ground the response, <b>augmenting</b> the capabilities of the AI model when it creates a response.

## Create Resources
To complete this exercise, the following resources are required:
<pre>
- An Azure OpenAI resource.
- An Azure AI Search resource.
- An Azure Storage Account resource.
</pre>

From the Azure Shell on the Azure Portal, the resources are then created with the following command:
<pre>
az cognitiveservices account deployment create \
   -g your_resource_group \
   -n your_OpenAI_resource \
   --deployment-name text-embedding-ada-002 \
   --model-name text-embedding-ada-002 \
   --model-version "2"  \
   --model-format OpenAI \
   --sku-name "Standard" \
   --sku-capacity 5

az cognitiveservices account deployment create \
   -g your_resource_group \
   -n your_OpenAI_resource \
   --deployment-name gpt-4o \
   --model-name gpt-4o \
   --model-version "2024-05-13" \
   --model-format OpenAI \
   --sku-name "Standard" \
   --sku-capacity 5
</pre>

## Call the Resources
To test  the sample code is cloned from GitHub at https://github.com/MicrosoftLearning/mslearn-openai
and the code is in the folder Labfiles/09-dalle-client. The code is executed locally in VS Code.
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/ownData.py
</br></br>
With Python projects, the .env file has to be updated with the keys and URL endpoints from both the Open AI and Azure Services.
</br>
When executing the Python code, and a question is answered at the prompt, the results are below:
<pre>
Enter a question:
Tell me about Las Vegas
{
  "id": "24f546d9-bbce-47cd-9d61-9deb0d7fb8d2",
  "choices": [
    {
      "finish_reason": "stop",
      "index": 0,
      "logprobs": null,
      "message": {
        "content": "Las Vegas, officially known as the City of Las Vegas, is the 28th-most populated city in the United States and the most populated city in the state of Nevada. It serves as the county seat of Clark County and anchors the Las Vegas Valley metropolitan area, making it the largest city within the greater Mojave Desert [doc2]. \n\nLas Vegas is internationally renowned as a major resort city, famous for its gambling, shopping, fine dining, entertainment, and nightlife [doc2]. The Las Vegas Valley as a whole is the leading financial, commercial, and cultural center for Nevada [doc2].\n\nMargie's Travel offers several hotel options in Las Vegas, including:\n- **The Volcano Hotel**: Located in the heart of The Strip, this stylish casino hotel features live entertainment and an extensive pool area [doc2].\n- **The Fountain Hotel**: A luxury accommodation with a range of restaurants and cocktail bars [doc2].\n- **The Canal Hotel**: An opulent Italian-themed resort with luxurious suite accommodation [doc2].\n\nFor more information or to book a trip to Las Vegas, you can visit Margie's Travel website at www.margiestravel.com [doc2].",
        "refusal": null,
        "role": "assistant",
        "audio": null,
        "function_call": null,
        "tool_calls": null,
        "end_turn": true,
        "context": {
          "citations": [
            {
              "content": "Wherever you want to go, Margie’s Travel can get you there! \n\nMargie’s Travel is a world-leading travel agency, combining international reach with local \n\nexpertise. Just tell us where you want to go, and we can arrange: \n\n• Flights \n\n• Accommodation \n\n• Transfers \n\n• Visas \n\n• Currency Exchange \n\n• Excursions \n\n \nWhere We Go \nWhile we can arrange travel to anywhere \nworldwide, we specialize in trips to: \n\n• Dubai \n\n• Las Vegas \n\n• London \n\n• New York \n\n• San Francisco \n\nWho We Are \nMargie’s Travel employs some of the \nbest travel experts in the world. Our \nleadership team consists of: \n\n• Marjorie Long (CEO) \n\n• Logan Reid (CFO) \n\n• Emma Luffman (CTO) \n\n• Deepak Nadar (Strategic Director) \n\n \n\nTo learn more about us, visit our website at www.margiestravel.com",
              "title": "Margies Travel Company Info.pdf",
              "url": null,
              "filepath": null,
              "chunk_id": "0"
            },
            {
              "content": "Margie’s Travel Presents… \n\nLas Vegas \n Las Vegas, officially \n\nthe City of Las Vegas \n\nand often known \n\nsimply as Vegas, is the \n\n28th-most populated \n\ncity in the United \n\nStates, the most \n\npopulated city in the \n\nstate of Nevada, and \n\nthe county seat of \n\nClark County. The city \n\nanchors the Las Vegas \n\nValley metropolitan \n\narea and is the largest \n\ncity within the greater Mojave Desert. Las Vegas is an internationally renowned major resort city, \n\nknown primarily for its gambling, shopping, fine dining, entertainment, and nightlife. The Las Vegas \n\nValley as a whole serves as the leading financial, commercial, and cultural center for Nevada. \n\nLas Vegas Hotels \n\nMargie’s Travel offers the \n\nfollowing hotels in Las \n\nVegas: \n\nThe Volcano Hotel \n\nIn the heart of The Strip. \n\nStylish casino hotel with \n\nlive entertainment and an \n\nextensive pool area. \n\nThe Fountain Hotel \n\nLuxury accommodation in \n\nLas Vegas with a range of \n\nrestaurants and cocktail \n\nbars \n\nThe Canal Hotel \n\nAn opulent Italian-themed \n\nresort with luxurious suite \n\naccommodation. \n\n \n\nTo book your trip to Las Vegas, visit www.margiestravel.com",
              "title": "Las Vegas Brochure.pdf",
              "url": null,
              "filepath": null,
              "chunk_id": "0"
            }
          ],
          "intent": "[\"Las Vegas overview\", \"Las Vegas history\", \"Las Vegas attractions\"]"
        }
      }
    }
  ],
  "created": 1746567845,
  "model": "gpt-4o",
  "object": "extensions.chat.completion",
  "service_tier": null,
  "system_fingerprint": "fp_ee1d74bde0",
  "usage": {
    "completion_tokens": 255,
    "prompt_tokens": 2849,
    "total_tokens": 3104,
    "completion_tokens_details": null,
    "prompt_tokens_details": null
  }
}

</pre>
