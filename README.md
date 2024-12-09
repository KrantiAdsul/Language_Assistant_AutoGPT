**Developed Language Learning Assistant using AutoGPT platform which helps translate given text from one language to another.**

•	Agent takes input from user which specified which language the user is planning to provide as an input.

•	Another input provided by user is the actual text which they want to be translated (here to French language)

**Observations:**

a.	Previously I created similar language assistant model using Langflow, and the main difference I observed was the number of blocks required on Autogpt was much higher than in Langflow. 

b.	Also, Autogpt is providing a much finer control over the way the input prompt will be designed, used and modified before providing it to the actual LLM model.

**Details of blocks used:**

i.	Agent input blocks – used to collect information about user inputs. Here I used two block – one for specifying what input language user is using and other to specify the actual text which needs to be translated.

ii.	Add to dictionary block -  used to add a new key-value pair to the dictionary – which in this case looks like:
{"User Language": "English",
  "User Input": "How to say good morning in French?"}

iii.	AI text generator block – used to call LLM model using the prompt generated here through ‘Add to dictionary block’ to generate required output string. LLM used here is again: GPT -4o.

iv.	Agent Output blocks – to display output of the agents – here the translation of good morning in French i.e Bonjour!

**Dependencies:**

You need to download and setup AutoGPT following steps listed on : https://agpt.co/blog/introducing-the-autogpt-platform
