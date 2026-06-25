## LLM Evaluation Workflow:

- This is the How Part means how we do the LLM Evaluations.

#### Take a scenario:
    - We are working in a company, they receive huge amount of emails and they want to automate it. They want the system to reads the emails, understand the content and do classification on the basis of content. Like if the customer asking for billing, technical, general. If the query is related to billing we route that to billing team and same for others. We want to automate this process.

    - We made a simple system:
        - There is an LLM that receives and routes that according to the content.
        - But now the real question is??
            - Is the system capable of doing this?
            - Should we directly deploy it?
            - The system should be evaluated first
            - Now look at the flow we are going to evaluate the system

## Workflow Steps:

### 1. Define Task & Target
- What you want to evaluate? Define that first. In our case, we are evaluating the above system and its classification.

### 2. Define a Success Critera
- Accuracy is require here. 80 % accuracy is good, 90% is better, 95 % is best. 
- The metric here is accuracy. What do you mean by accuarcy?? If the model correctly classify that e-mail. 

### 3. Build a Dataset.
- We need to prepare a dataset that have inputs and expected outputs. 
- In our case, Input is the email content. Expected output is the classification. 
- For Example:
    - Input Messages and Expected Label:
        - My Card was charged twice -> Billing
        - The app crashes on login -> Technical
        - What are your hours -> General

- Generally, we need to have 50 to 500 rows of dataset, which can be used for evalution.
- We should have past real data and create the dataset on which we evaluate our application. This dataset is called Golden Dataset.

### 4. Define an Eval Method
- You decide who is going to evaluate? Automatic, Humand or LLM. 
- We send our dataset to the system and our system tells the answers for the emails. We then check the accuracy.
- For this task, we need to have a way or method. For this case, we can use a python script and we have a method of Automatic. 
- In production applications and RAG Applications, we use LLM as a Judge concept where a good LLM models checks the answer. We send our LLM as a Judge the user query, AI Answer and retreived chunks. 

### 5. Run The Model
- Run the model on the dataset and collect results.

### 6. Evaluate the Results.
- We have automated method and our python is calculating the accuracy. Suppose Our accuracy is 80 %. 
- Now, if we are satisfied with the results, we can deploy it. But 80 % is not good for a production model. 

### 7. Analyze the result
- You think where the mistake happened. You look for the scope of improvement. 
- What is the thing we can change and improve the accuracy?
    - We can change the prompt, change the LLM, change the embedding model, change the retriever, change the chunking strategy, change the system instruction, etc.
- We try to improve the system in this step.

### 8. Iterate
- After making the changes, we run the evaluation again.
- We repeat this cycle until the accuracy is satisfactory.
- See we made changes and we have the golden dataset, we have made changes, we iterate and check the accuracy again. The accuracy is now 90 to 95%
- Now you reach a step where you think you can deploy the system

### 9. Deploy & Monitor:
- After deploying, you continously monitor the system.
- Keep evaluating the system time to time with the same dataset.
- We had accuracy of 95% onto our dataset. We need to check the performance of the system in production.

### 10. Production Failures:
- We keep the track of failures and all, we add the failed emails on our golden dataset and made changes again and iterate. Our dataset keeps getting richer and improved and our system improves over time. 

### This is the same flow applies to RAG, Agents and LLM Based Applications. 



