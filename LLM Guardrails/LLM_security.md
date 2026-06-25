# LLM Guardrails:

- What makes an application secure? By adding security layers.
- No matter what happens, peoples cannot break it and go through your system. So this way your LLM Based Applications should be secure.
- Prompt Injection, Sensitive Topic, Dialogues, Jailbreak (Users trying to override the system prompt and trying to make the LLM do something against the rules)
- In order to avoid these things, we need to secure our LLM's.
- We dont want waste our token on Dialogues things (normal, hi, bye, greetings).
- Observability means tracking every step of your LLM applications. 

## We add a layer of security over our LLM's. This is called as LLM Guardrails.

- The moment user query enters the system, the guardrails checks if the answer is secure or not. Then after sending the final answer, we again check if the answer is secure or not using Guardrails. This checks include if LLM's include any personal information or not.

- We need to make sure that our system is Robust, Fault Tolerant, secured. To make it fault tolerant, we use LLM gateways.

- The context is to make it secure, we are using Guardrails. This means we are guarding our application. Guard means Protecting, Guarding our system and Rail means Rules and Regulations.
- Just like we set up rules and regulations for the bodyguard like do not harm, do not reveal, for example real life bodyguard, we tell him to go there always, check it always, etc.

### Input Guardrails:
- Lets say we are applying Intent layer which classifies if the query is Prompt Injection, Jail Breaking, Sensitive Topic or not, if its we would not reply it. 
- If its not we reply it. Thats our security layer. We keep adding layers on our LLM applications.

### Output Guardrails:
- Output Sanitizer: 
    - Basically after LLM response, we check the output and classify it.
    - If its safe, we send it to user. If not we block it.

## To integrate Guardrails in your Applications, you have different frameworks:

### 1. Nemo Guardrails

### 2. Guardrails AI

### 3. LLama Firewall / Guard

### 4. AWS Bedrock Guardrails

- You can decide the framework based on your needs and based on the preferences and use cases.

## Nemo Guardrails

- We are going to use and learn about this framework.
- It is developed by Nvidia and a production ready framework.
- Nemo Guardrails help us to write Rails.
    - Rails means Rules and Regulations using expression language Colang.
    - These Colang (.CO files) are passed to our LLM. 
    - We write Rules and Regulations in .co files.
    - It is a expression language developed by nvidia and it has only 3 keywords.
        - Define User
            - User should say these things.
        - Define Bot
            - Bot should say these things.
        - Define Flow
            - 
## Overview of .co File:

- Define User, Bot, Flow.
- Define User (Off Topic).
    - Meaning we are telling that user can say these things Tell me a joke, tell me how to make coffee.
- Define Bot (Off Topic).
    - Meaning bot can go off topic, we need to restrict this.
- Define Flow
    - If user is off topic, bot will refuse off topic. (This is just an example)

## Actual Code of Colang file:
#### define user off topic
    - "tell me a joke"
    - "what is the capital of france"
    - "write me a poem"

### define bot refuse off topic:
    - "I am an enterprise IT Assistant focused on Kubernets"

### define flow handle off topic:
    - "user ask off topic"
    - "bot refuse off topic"
    - "stop"

## The question is How the Intention is Detected then??
- We defined a rail. When we define a rail, a user might say these things. (Example above)
- The moment the new query comes or sends a new query, the query will be converted into a vector and all the above examples of the rails are converted into embeddings, then it looks for similarity. This is how it is working and handling. It is a simple and easy process and happens with Fast Embed. 