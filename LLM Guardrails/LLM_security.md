# LLM Guardrails:

- What makes an application secure? By adding security layers.
- No matter what happens, peoples cannot break it and go through your system. So this way your LLM Based Applications should be secure.
- Prompt Injection, Jailbreak (Users trying to override the system prompt and trying to make the LLM do something against the rules)
- In order to avoid these things, we need to secure our LLM's.

## We add a layer of security over our LLM's. This is called as LLM Guardrails.

- The moment user query enters the system, the guardrails checks if the answer is secure or not. Then after sending the final answer, we again check if the answer is secure or not using Guardrails. This checks include if LLM's include any personal information or not.

- We need to make sure that our system is Robust, Fault Tolerant, secured. To make it fault tolerant, we use LLM gateways.

- The context is to make it secure, we are using Guardrails. This means we are guarding our application. Guard means Protecting, Guarding our system and Rail means Rules and Regulations.
- Just like we set up rules and regulations for the bodyguard like do not harm, do not reveal, for example real life bodyguard, we tell him to go there always, check it always, etc.

## To integrate Guardrails in your Applications, you have different frameworks:

### 1. Nemo Guardrails

### 2. Guardrails AI

### 3. LLama Firewall / Guard

### 4. AWS Bedrock Guardrails

- You can decide the framework based on your needs and based on the preferences and use cases.

## Nemo Guardrails

- We are going to use and learn about this framework.
