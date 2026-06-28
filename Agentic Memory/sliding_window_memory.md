## Sliding Window Memory
- The main idea here is that instead of appending and sending every message in the list, we just send N number of messages to LLM like last 4 turns or last 4 past interactions.
- Although this majorly solves the token problem as compared to conversation buffer memory but the main drawback is the fact that you lose the important context of early messages. 
- If the user asks something which you did not pass to LLM, the LLM wouldn't know that. Let's say users tell his name in the first turn and in the 10th turn, you did not send the first turn message, the LLM would forget the name of the user.

## The Window is defined in turns, not tokens
- A turn is one user message plus one assistant response (2 messages). A window of k=5 keeps the last 5 completed turns. This is more intuitive to reason about than raw token counts.

### Old Messsages are not deleted - They are evicted from the active window

- Evicted means not deleted. They must be somewhere. It is homework to know that where it went.   

- This is the forgetting problem
- The solution? Combining sliding window with entity memory or vector retreival. 

### The Critical Trade off - Recency vs Completeness

- The buffer remembers everything. The window remembers only the recent past. 
- This is the fundamental limitation of sliding window memory, it solves the cost problem but introduces a forgetting problem. 
- Its like RNN problem. 
 

## Production Verdict:
- Viable as the short term layer of a larger memory system. Not sufficient alone.
- It is almost present in production systems but almost never alone. It is paired with a long term retrieval layer (vector store, knowledge graph). that catches the facts that slides out of the window. 

  