# Azure Video Indexer

The Azure Video Indexer has many capabilities, which allows the extraction of custom insights from videos. 
Once a vidoe is indexed, it be embeded within widgets on an HTML page and API can be called to retreive information.
</br></br>
The Video Indexer portal is at https://www.videoindexer.ai
</br>
The video at at https://aka.ms/responsible-ai-video will be downloaded locally, and uploaded to the Video Indexer portal.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexPortal.png"/></p>
The indexing process extracts insights from the video, which you can be viewed in the portal.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexUploaded.png"/></p>
In the timeline tab, different views can be applied for custom views.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexTimeline.png"/></p>
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexTimeLineViews.png"/></p>
Key words can be used to search and filter.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexTimelineFilters.png"/></p>
To call the API, the code is at https://github.com/MicrosoftLearning/mslearn-ai-vision under the folder 06-video-indexer folder
</br>
The following PowerShell script will need to be updated.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexAPICall.png"/></p>
The account ID is retried from the Video Index portal account settings. The API key is retrieved from the portal  https://api-portal.videoindexer.ai in the profile settings.
<p><img src="https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Images/Vision/VideoIndexPortalDev.png"/></p>
REST API can be used to work with videos in the account. For this step, a PowerShell script is used to make REST calls; but the same principles apply with HTTP utilities such as cURL or Postman, or any programming language capable of sending and receiving JSON over HTTP.
</br>
</br>
Results of the powershell script will look like this:</br>
<pre>
{
    "results":  [
                    {
                        "accountId":  "ACCOUNTID",
                        "id":  "ID",
                        "partition":  null,
                        "externalId":  null,
                        "metadata":  null,
                        "name":  "responsible_ai",
                        "description":  null,
                        "created":  "2025-04-08T21:27:24.36+00:00",
                        "lastModified":  "2025-04-08T21:30:15.3933333+00:00",
                        "lastIndexed":  "2025-04-08T21:30:15.3933333+00:00",
                        "privacyMode":  "Private",
                        "userName":  "First Last",
                        "isOwned":  true,
                        "isBase":  true,
                        "hasSourceVideoFile":  true,
                        "state":  "Processed",
                        "moderationState":  "OK",
                        "reviewState":  "None",
                        "isSearchable":  true,
                        "processingProgress":  "100%",
                        "durationInSeconds":  114,
                        "thumbnailVideoId":  "ww8ku7bc9r",
                        "thumbnailId":  "8e961dbd-edbc-452e-9b2d-cceb7188ce92",
                        "searchMatches":  [


                                          ],
                        "indexingPreset":  "Default",
                        "streamingPreset":  "SingleBitrate",
                        "sourceLanguage":  "en-US",
                        "sourceLanguages":  [
                                                "en-US"
                                            ],
                        "personModelId":  "00000000-0000-0000-0000-000000000000"
                    }
                ],
    "nextPage":  {
                     "pageSize":  25,
                     "skip":  0,
                     "done":  true,
                     "totalCount":  1
                 }

    </pre>
