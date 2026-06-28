## Summary Buffer Memory
- A hybrid memory that keeps recent messages word-for-word while summarizing older history.

- It is keeping recent messages (verbatim) but older messages going to be summarized and put in history. The context depends on the recent messages and the summarized messages. 

- It is a hybrid of Short Term and Long Term Memory. 

#### Summary Buffer Memory is a hybrid agent memory technique that combines conversation buffer and summary memory into one system. It keeps recent messages word-for-word while compressing older conversation history into a running LLM-generated summary. 

- This is exactly how humans manage conversations - we don't recall every word from 10 turns ago, but we keep a running summary of what matters. 

- It works by keeping a "buffer" of the most recent messages in raw format. Once the buffer reaches a certain size (e.g., 10 messages), it uses an LLM to create a concise summary of those messages. This summary is then prepended to the memory, effectively compressing the conversation history.

- It can be used for medium scale applications or medium scale enterprise applications. 

- The engineering challenge is tuning the transition threshold. If it is too low, it will be too expensive. If it is too high, it will be too slow.

- 
