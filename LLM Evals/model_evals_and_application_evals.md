
## LLM Evals are mainly divided into two parts:
### 1. Model Evals
### 2. Application Evals

## Model Evals:
- Model evals are those evals on which we evalute our LLM models.
- Model evals evalute the model itself. The main idea is to test and evaluate the capabilities of a model 
- We test the capability of a model on the different benchmarks such as MMLU, Reasoning, Maths, SWE and all.
- Basically, benchmarks are evals defined already and whenever the new LLM comes, we test the LLM on those benchmarks.

### Capabilites of a Model:

- 1. Reasoning?
    - Can it reason?
- 2. Knowledge:
    - Can it answer knowledge-based questions?
- 3. Maths
    - Can it solve maths problems
- 4. Coding
    - Can it write code
- 5. Instruction and Following
    - Can it follow the instructions?
- 6. Long Context:
    - Can it follow long documents?
- 7. Multiomodal Understanding: 
    - Does it understand images, audios, videos?
- 8. Tool-Use:
    - Can it use tools?

## Examples Benchmarks:
- 1. General Knowledge + Reasoning Benchmark: **MMLU**
    - Broad subject knowledge and reasoning across many domains

- 2. Maths: **GSM8K**
    - Grade school math word problems

- 3. Coding: **HumanEval, SWE-Bench**
    - Code Generation and real-world software engineering issue solving.

- 4. Instruction Following:  **IFEval**
    - Whether the model follow explicit constraints and formatting instructions

- 5. Long Context: **Needle-in-a-Haystack**
    - Measures recall in long context windows (finding a specific fact in a long document)

- 6. Multimodal Capabilites: **MMMU**
    - Reasoning Over Images, diagrams, charts, and visual academic problems. 

## Key Points:
- Model Evals are not done by us, it is done by Frontier Labs such as Claude, OpenAI, Gemini. 
- We just know what are models evals and what are the benchmarks, so that in future we are making an LLM applications and we have good knowledge of Model Evals and benchmarks, we will be able to decide the best LLM for our use case. 

## Application Evals:
- This is the category we should be focus on being an AI Engineer and this is what we apply in our LLM applications. 
- In LLM Applications, LLM is just a single component, we have the whole harness layers and other components which are very important such as:
    - Prompt Layer
    - Tools / API's
    - Orchestrator / Workflow
    - Guardrails / Safety
    - Output Parser
    - Context / Memory
    - Retrieval System
    - Embedding Model
    - Vector Database
    - Monitoring / Logging
    - Feedback Loop
    - Observability 


   

