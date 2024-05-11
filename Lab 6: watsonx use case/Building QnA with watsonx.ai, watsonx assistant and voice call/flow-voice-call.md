# watsonx flow with Phone Voice Calls
in order to make the flow is seamless, it necessary to make sure the flow is expected as we need. There are several intent that we will make, such as greetings, introduction, retrieve to knowledge, and connect with the live agent


First, you need to upload OAS for call watsonx and watsonx discovery API in the integration tab
[Upload OAS file name watsonx-openapii.json](https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/blob/main/Lab%206%3A%20watsonx%20use%20case/Building%20QnA%20with%20watsonx.ai%2C%20watsonx%20assistant%20and%20voice%20call/watsonx-openapii.json) and [Upload OAS file name watson-discovery-query-openapi.json](https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/blob/main/Lab%206%3A%20watsonx%20use%20case/Building%20QnA%20with%20watsonx.ai%2C%20watsonx%20assistant%20and%20voice%20call/watson-discovery-query-openapi.json)

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/0528cecc-f33f-4378-8f98-4f115f9869c8">


Second, you need to upload phone-action.json in the global setting. Once you uploaded, the flow will be automatically created
[Upload action file name Phone-action.json](https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/blob/main/Lab%206%3A%20watsonx%20use%20case/Building%20QnA%20with%20watsonx.ai%2C%20watsonx%20assistant%20and%20voice%20call/Phone-action.json)

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/cb3a75da-ff4a-497d-83c6-536eca45a166">


## Greet customer
For the voice call, it is necessary to put conditions "Channel Name" to "Phone" as the first thing that the bot will welcome you

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/5da3cce4-9501-464d-bf25-dbe9ea46820e">


You can adjust variations response to make a variation response
<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/64b05e5c-0b22-4a6b-af93-dfbe0acdfabf">

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/692bc89a-d55b-4684-bd53-9196eae515ce">


Then, whenever the user say something we will direct it to either one of this 4 actions; introduction, policy, end_conversation, and agent


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/e1070c0d-5e13-4504-965d-3327005ef511">


## Introduction
In the introduction part, when the user gently greets the bot like say "hello" or "assalamulaikum". The bot will understand and saying "is there any help?"

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/cd755a7e-40a3-459e-bd9f-e1a7764f412b">


## policy
In the policy part is the place where we need a knowledge about the leave company policy. It is where we need the watsonx ai and watsonx discovery for generate the response.

First we need to put the intention, if user asking about the policy or leave company. The assistant will proses in this flow.


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/518b3211-8d59-4d54-9d63-5ab0a76f20e9">


Everytime we say over the phone, there is session history that can keep the conversation. We set the variable for the first_invokation for the question that we need on watson discovery and watsonx ai part


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/25a2fd27-5531-4298-9a38-6eb15ae8335b">


We use extension for watson discovery for the step 2


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/94654956-d4de-44f6-8f2b-f386e1fe808f">


In the step 3, we save the output of watson discovery where this ouput contain a retrieval of document that we searched

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/ced7269e-9b9f-4771-bbdd-a99adc0fbe2b">


In the step 4, use the watsonx ai extension to generate the passage from the document retirival based on the question

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/89614743-bdde-4dee-b217-6c3b1a3a9efa">


You can easily put an instruction and adjust the prompt for the ai


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/b22b9d0b-ffe1-4479-9438-46e1248a5073">


In the last step, this is where the output of watsonx ai is generated


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/18039bfb-e807-436f-bd03-7134ad425f8c">


## Live Agent
In this intent action, this is where when we need to put live agent in phone. When user wanted to direct to the live agent itself.


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/822e86f1-639e-42fa-978e-bda815d19756">

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/a7e14914-0d35-4f14-8404-c3b93b2c0c72">


## End Conversation
This is the place where we want to end the call where it is enough to call with the assistant. If you remember in the "policy" action. Everytime we asked, always get an question back to the user "is it enough or is there anything that I can help"

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/a0631fea-9cd4-4cc3-86a7-d3258865ce35">


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/93fcc58f-b09d-489f-af4c-41159103b23b">






























