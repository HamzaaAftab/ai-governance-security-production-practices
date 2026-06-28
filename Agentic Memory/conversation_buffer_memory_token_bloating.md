## Conversation Buffer Memory
- Simple meaning is List or List of Messages.
- The main idea was that:
    - LLM's are stateless and they cannot remember and recover information, previous interactions. 
    - This is not a bug, it's a feature. It's an isolation.
    - Buffer is a list, you append the message everytime you interact with the LLM's so that LLM's remembers what happened in the conversation.
    - Messages include: User Messages, AI Messages, System Messages and Tool Messages. (Tools Messages are in Agentic Systems)
    - This is the most simplest memory strategy. This is the simplest solution to statelessness problem. We Keep appending messages in the list and send to LLM's.
    - #### Examples to understand the Turns:
    - Turn 1 -> send: [system, user_msg_1]
    - Turn 2 -> send: [system, user_msg_1, assistant_msg_1, user_msg_2]
    - Turn 3 -> send: [system, user_msg_1, assistant__msg_1, user_msg_2, assistant_message_2, user_msg_3]
    
***Look at the pain point here at the conversation buffer memory:***
    - We are sending the same messages again and again and again. With increase in number of turns, the number of messages keep increasing and token keep increasing. 
    - This is called Token Bloating.

- Each Message has a role. Role Order is Strict
    - System
    - User
    - Assistant

***The Model does not remembr anything. You give it the transcript. It reads it. That is the entire mechanism***

#### Token cost grows with every turn. This is the fundamental pattern. 
- Turn 1: 50 Tokens
- Turn 2: 130 Tokens
- Turn 3: 450 Tokens
- Turn 10: 950 Tokens

- Per turn cost grows linearly. Total conversation cost grows quadratically. At scale with thousand of users, this is a serious unit-economics problem. \

## Think about it this way:
- Scale this. Turn 50, 10,000 users.
- Turn 50 sends 8,000 tokens - 160x more than turn 1.
- A power user with 200 turns can hit 30,000+ tokens per call.

#### The Context Window is the hard ceiling. Hit it and call fails. 

## Production Verdict:
- Not sufficient alone. Always present as a component.
- No production system uses raw buffer memory as its only memory layer. But every production system uses something like a buffer for the current active session - bounded by a hard token budget, persisted to a database, and supplemented by a long term memory layer for returning users. 

## This is the drawback of Conversation Buffer Memory.
