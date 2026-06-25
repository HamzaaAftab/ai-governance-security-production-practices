
## LLM Evals:
- LLM evals are systematic, repeatible tests used to judge an LLM or LLM powered system against a clear criteria.

### Systematic:
- It is not vibe testing.
- Here you create a dataset where you try to create every edge case on which you can your LLM. 
    - For example, 100 questions you think your users will ask. Real world behavior testing of your LLM application.

## Repeatable:
- If we change the prompt, model, retriever, chunking strategy, or system instruction, we should be able to run the same test again and compare results.
- This is how we know whether the system improved or became worse. 

## Clear Criteria:
- We must define what good means. 
    - Correct
    - Simple explanation
    - Grounded in course content
    - Safe and policy-compliant. 

- Without critera, we are only judging by vibes.

#### LLM evals are basically tests for LLM powered applications where you check your LLM on the basis of criteria.

- An Eval is not just a metric. An eval is the complete testing setup. It includes
    - What are we evaluating?
    - What does good mean?
    - What test cases are we using?
    - How are we judging the output?
    - When are we running it?
    - Which tool are we using?

- We are talking about the complete process of testing an LLM-powered system in a structured way. 

## Remember LLM Evals are not just metric, but it is a complete testing setup for LLM Application.
    - Lets say we are evaluating RAG Application, and we want to evaluate our retriever, then it is the part of our evaluation. 

## The goal is not just to get a score. The goal is to answer practical questions like:
    - Can the model be used for a particular task / application? 
    - Is this system good enough to ship?
    - Did prompt v2 improve over prompt v1?
    - Is the RAG answer grounded in the retrieved context?
    - Is the agent completing the task correctly?
    - Is the chatbot safe for real users?
    - Does my LLM app provide factual answers?
    - Is the latency under control?

    