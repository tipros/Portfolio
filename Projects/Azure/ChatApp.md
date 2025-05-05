# Generative AI chat app

In this project, the Azure AI Foundry SDK is used to create a simple chat app that connects to a project and chats with a language model.


## Create Project
From https://ai.azure.com, a new project is created. A wizard will guide through the creation of the new project and hub.
</br>
Deploy a new model and select gpt-4o. 

## Call Speech Translator Service
To test  the sample code is cloned from GitHub at https://github.com/microsoftlearning/mslearn-ai-studio mslearn-ai-foundry 
and the code is in the folder mslearn-ai-foundry/labfiles/chat-app/python. The code is executed directly from the Azure portal through **Cloud Shell**.
</br></br>
The updated Python code can be found at https://github.com/tipros/Portfolio/blob/main/Projects/Azure/Code/chat-app.py
</br></br>
With Python projects, the .env file has to be updated with the HUB connection string and name of deployment.
</br>
When executing the Python code, chat bot will prompt the user. Sample conversation below:
</br>
<pre>
Enter the prompt (or type 'quit' to exit): What is the fastest animal on Earth?
The fastest animal on Earth is the **peregrine falcon** (*Falco peregrinus*). This remarkable bird achieves its incredible speed during a hunting dive, known as a **stoop**, where it can reach speeds of up to **240 mph (386 km/h)** as it plunges toward its prey. 

If we consider horizontal speed, the **Brazilian free-tailed bat** (*Tadarida brasiliensis*) and several species of birds like the **common swift** (*Apus apus*) are among the fastest, capable of reaching sustained speeds of over **60 mph (97 km/h)**. For terrestrial animals, the **cheetah** (*Acinonyx jubatus*) holds the title, capable of running up to **60-70 mph (97-113 km/h)** for short distances.
Enter the prompt (or type 'quit' to exit): Where can I see one?
You can see a **peregrine falcon** in many parts of the world, as it is one of the most widespread birds of prey and is found on every continent except Antarctica. Here are some places and tips to observe them:

### 1. **Urban Areas**
Peregrine falcons are known to nest on tall buildings, bridges, and skyscrapers in cities because these mimic the cliffs they traditionally nest on. Major cities like **New York City**, **London**, **Chicago**, and **San Francisco** often have peregrine falcon sightings. Some cities even offer webcams to watch their nesting sites live during breeding season.

### 2. **Naturally Wild Habitats**
They can also be spotted in more remote, natural areas:
- **Cliff faces, mountains, or rocky coasts**: Peregrine falcons historically nest in these habitats. Locations such as the **Grand Canyon** (USA), **Scottish Highlands**, or **Yosemite National Park** are excellent places to spot them.
- Open landscapes like **grasslands**, **deserts**, or **river valleys**.

### 3. **Migration**
During migration seasons (spring and fall), peregrine falcons often pass through **bird migration hotspots**, such as:
- **Cape May, New Jersey (USA)**
- **Point Pelee National Park, Ontario (Canada)**
- **Falsterbo, Sweden**

### Tips for Spotting Peregrine Falcons:
- Visit in the **early morning** or **late afternoon** when they are most active.
- Use binoculars or a spotting scope for better viewing.
- Look for their characteristic hunting dives, and listen for their sharp, high-pitched calls.

If you're in an urban area, research if local conservation groups or birdwatching societies track peregrine falcons. They often provide information on nest locations or organized tours. Happy birdwatching!
Enter the prompt (or type 'quit' to exit): Are they endangered?
The **peregrine falcon** (*Falco peregrinus*) is **not currently endangered** on a global scale. In fact, thanks to conservation efforts, its populations have recovered significantly in many areas where they once faced serious declines.

### Conservation Status:
- According to the **International Union for Conservation of Nature (IUCN)**, the peregrine falcon is classified as **Least Concern**, meaning it is not considered at risk of extinction globally. 
- In some regions, however, local populations may remain vulnerable due to specific threats.
---
### Why Peregrine Falcons Were Previously Endangered:
In the mid-20th century, peregrine falcon populations declined drastically, especially in North America and Europe, due to widespread use of **pesticides** like **DDT**. DDT caused thinning of their eggshells, leading to high rates of egg mortality. By the 1970s, peregrines were considered endangered in many areas.
---
### Recovery Efforts:
Peregrine falcons made an incredible comeback thanks to conservation efforts, including:
1. **Banning DDT**: The United States banned DDT in 1972, allowing bird populations to recover.
2. **Captive Breeding Programs**: Birds were bred and released into the wild to reestablish populations.
3. **Protection Laws**: They were granted legal protection under acts like the **Endangered Species Act** in the U.S.
4. **Artificial Nesting Sites**: Urban environments have been adapted to provide nesting spaces like rooftops and man-made ledges.
---
### Current Challenges:
While no longer endangered, peregrine falcons still face threats, including:
- **Habitat destruction**
- **Climate change**
- **Collisions with structures** in urban areas
### Celebrating Their Success:
The recovery of the peregrine falcon is often cited as one of the world’s greatest conservation success stories. Today, you can see them thriving in many parts of their range across cities and natural habitats!
Enter the prompt (or type 'quit' to exit): quit
  </pre>
