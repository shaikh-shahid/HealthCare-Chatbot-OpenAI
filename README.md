## Objective
To help design a chatbot using OpenAI that helps identify the health issue the user is facing and upon finding the issue, extract the advice from the local store recommendations from the certified doctors. 
As this is a health problem, we can’t rely on bots to give medical advice.

## System Design

![image](/chatbot%20design.jpg)

The design is simple, we aim to take the user input by welcoming the user with greetings and asking if they are facing any problems. 
Upon receiving the problem, if the problem is clear, we categorize the problem into health issues fetched from the dataset. If not, ask more questions to get a better understanding. 
Once the health issue is found and categorised, we will look into our dataset and extract the solution. If the category is not present, we ask more in-depth questions to categorize the problem. 
When a user types “exit”, we terminate the bot.

## Solution

I am using a dataset from Kaggle that has health issues and their solutions listed in it. I am using OpenAI to fetch the health issue and categorize it into the category. Here are some categories, ‘Cuts', 'Abrasions', 'stings', 'Splinter', 'Sprains', 'Strains', 'Fever', 'Nasal Congestion', 'Cough', 'Sore Throat', 'Gastrointestinal problems', 'Skin problems', and more.

## Usage of Function calling
In this problem set, I have not found a concrete use case for the function calling but putting a simple example of how I can use it if I want to expand it a little further. I plan to use function calling if the problem is found and we ask the location of the user to fetch good doctors near the user using Google Places API.
