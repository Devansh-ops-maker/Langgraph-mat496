# Langgraph Project

**Author:** Devansh Singh (2410110755)

---

## Learnings from Module 1(Course 1)

- Learned how to make a simple graph.  
- Understood the concept of **states**, which hold the data passed between nodes and ensure every function knows what kind of data it is receiving and returning.  
- Each **node** is a small function that takes the current state, modifies it, and returns the updated version.  
- **Edges** tell the graph how the nodes are connected.  
- The **StateGraph** class helps in building this pipeline and managing the flow between nodes.

---

## Changes Implemented in Module 1 (Course 1)

- Created a graph with **five nodes**, representing a simple flow of sentences.  
- Implemented a **linear sequence of nodes**, instead of conditional edges, where each node updates the text state.  
- Final output forms a smooth message by passing the state sequentially through all nodes until reaching the `END` node.

---

## Learnings from Module 1 (Course 2)

- Learned how to create **messages** that capture different roles (`AIMessage` and `HumanMessage`) and use them in chat models.  
- Chat models can take multiple messages as input and generate follow-up responses based on conversation history.  
- Learned how to **bind tools with an LLM**, enabling the model to perform specific tasks programmatically.  
- Explored using **messages as the graph state** and integrating **MessageState** with the graph for dynamic conversation flows.

---

## Changes Implemented in Module 1 (Course 2)

- Implemented a **coding-related conversation** graph where the LLM responds contextually to programming questions.  
- Created a **factorial tool** and bound it to the LLM, allowing the graph to perform computations dynamically based on user input.  
- Enhanced interactivity and versatility, enabling the graph to handle coding queries and execute functions while maintaining conversation context.

---

## Learnings from Module 1 (Course 3)

- Learned how to implement a **router in Langgraph** to decide how to respond to a user.  
- Router can either return a direct **LLM response** or evaluate the LLM's output and call a **tool** to generate the correct response.  
- Enables dynamic decision-making within the graph based on conversation context.

---

## Changes Implemented in Module 1 (Course 3)

- Implemented a graph with a **factorial tool** integrated.  
- Graph first asks the LLM for a response when a user provides input.  
- Router **judges the LLM's response**; if inappropriate, it calls the factorial tool to provide a correct answer.  
- Made the graph **interactive and reliable**, combining LLM flexibility with deterministic tool execution.

---

## Learnings from Module 1 (Course 4)

- Learned how to use a **graph to interact with an LLM** dynamically.  
- Graph sends user input to the LLM, and if output is not appropriate, a **tool is called** to generate the correct response.  
- Tool output is passed back to the LLM, looping until a **suitable response** is obtained.  
- Demonstrates a **ReAct-style architecture**, enabling multi-step reasoning and dynamic decision-making.

---

## Changes Implemented in Module 1 (Course 4)

- Implemented a graph with **multiple string manipulation tools** bound to an LLM.  
- Graph evaluates the LLM output and selectively calls the appropriate tool based on user input.  
- Ensures **accurate and contextually appropriate responses**, leveraging both LLM reasoning and deterministic tool execution.

---

## Learnings from Module 1 (Course 5)

- Explored **ReAct-style design for Langgraph graphs**.  
- Learned to bind multiple tools to an LLM and dynamically evaluate user input based on **LLM output** and **tool execution**.  
- Implemented **memory management** to save interactions, enabling multi-step reasoning and maintaining context across multiple messages.

---

## Changes Implemented in Module 1 (Course 5)

- Created **multiple string manipulation tools**, including reversing strings, converting to uppercase, and counting vowels.  
- Implemented a **ReAct-style graph** that binds these tools with an LLM, allowing the system to decide whether to respond directly or call a tool.  
- Incorporated **threaded memory**, so each conversation thread preserves context and previous outputs, ensuring consistent and context-aware responses across multiple interactions.
---

### Learnings from Module 2 (Course 1)

- Learned how to define and use **custom state classes** in Langgraph, including `TypedDictState`, `Dataclass`-based states, and `Pydantic` models.
- Understood how these state classes can be **integrated with the `StateGraph`**, allowing nodes to receive and return strongly-typed data.
- Gained insight into how **typed states improve graph clarity and reliability**, ensuring that each node knows exactly what kind of data it is handling.

### Changes Implemented in Module 2 (Course 1)

- Implemented a **coding language state class** using `TypedDictState` and integrated it into a Langgraph `StateGraph`.
- Created a **chess move state class** using Python `Dataclass` and used it in a graph to model chess strategies.
- Developed a **school board state class** with `Pydantic` validation to represent students and their respective boards (CBSE/ICSE), and integrated it into a `StateGraph`.
- Demonstrated how to **leverage different state types** to build flexible, type-safe, and interactive graphs in Langgraph.

---

## Learnings from Module 2 (Course 2)

- Learned how **branching** can raise errors when multiple nodes overwrite the same state in one step.  
- Explored **reducers** to safely manage state updates.  
- Implemented **custom reducers** for more control.  
- Learned advanced **message handling tricks**:  
  - Adding messages  
  - Overwriting messages by ID  
  - Deleting messages  
- Used **`message_reducer`** to apply these tricks safely in conversation flows.  

---

## Changes Implemented in Module 2 (Course 2)

- Demonstrated **TypedDict** as a **StateSchema**.  
- Implemented branching with a **shopping cart example**, showing state conflicts.  
- Fixed branching errors using **annotated lists** with built-in reducers.  
- Extended fixes using **custom reducers**.  
- Created a conversation flow demonstrating all message tricks: **add, overwrite, delete**.  
---

## Learnings from Module 2 (Course 3)

- Learned the difference between **private state** and **overall state**:  
  - **Private state** is used for intermediate logic within the graph.  
  - **Overall state** is used for the final output of the graph.  
- Learned how to define **explicit input and output schemas** instead of using a single schema for the entire StateGraph.  
- Understood how separating states and schemas improves clarity, modularity, and type safety in complex graphs.  

---

## Changes Implemented in Module 2 (Course 3)

- Implemented **private and overall state** using a chess-related example.  
- Demonstrated the use of **multiple schemas** with a laptop purchase scenario.  
- Showcased how explicit input/output schemas and private state help manage intermediate logic without affecting the final output.  
---

## Learnings from Module 2 (Course 4)

- Learned how to use **messages as a State** in LangGraph.  
- Revised the concept of **`message_reducer`** to safely manage message updates within conversation flows.  
- Explored advanced message-handling techniques such as:  
  - **Filtering messages** before sending them to the LLM to include only relevant context.  
  - **Trimming messages** using `trim_messages()` to manage token limits efficiently.  
- Understood how these techniques optimize LLM calls, preserve essential context, and reduce unnecessary token usage.

---

## Changes Implemented in Module 2 (Course 4)

- Implemented a **JEE-related conversation** demonstrating the use of messages as a State.  
- Applied **message management techniques** (filtering and trimming) within this conversation between the human and the LLM model.  
- Showcased how these techniques improve conversation efficiency, maintain focus on recent context, and ensure concise and contextually relevant responses from the model.

---

## Learnings from Module 2 (Course 5)

- Used messages as the graph state for dynamic conversation handling.
- Implemented conversation summarization to maintain context.
- Managed memory across threads for independent conversation sessions.
- Applied message manipulations like trimming and deleting old messages.
- Used conditional graph flows to decide between summarizing or ending a conversation.
- Learned best practices for state management to enable multi-step reasoning.

### Changes Implemented in Module 2 (Course 5)

- Created a threaded animal chatbot for independent conversation sessions.
- Implemented memory with summarization to keep track of conversation context.
- Filtered and deleted older messages dynamically to reduce LLM prompt size.
- Added conditional flow to summarize conversation when messages exceed a threshold.
- Enabled interactive conversation where the model responds contextually.

---

## Learnings from Module 2 (Course 6)  

- Managed thread-safe state updates across multiple conversation threads.  
- Implemented context-aware decision logic for dynamic graph flows.  
- Applied advanced message transformations, including formatting, filtering, and enriching messages before sending to the LLM or tools.

---

### Changes Implemented in Module 2 (Course 6) 
- Built a book recommendation assistant providing contextual suggestions.  
- Added conditional nodes to fetch recommendations, ask clarifying questions, or summarize conversations.  
- Integrated threaded memory for independent conversation threads.  
- Applied message manipulations: trimming, filtering, summarizing old messages.

---

## Learnings from Module 3(Course 1)

- Learned about **LangGraph Dev** and its role in building and visualizing conversational workflows
- Understood how **threads, runs, and streaming** contribute to real-time interaction tracking
- Explored **event-based message handling** for creating dynamic and stateful AI behavior

---

### Changes Implemented in Module 3(Course 1)

- Integrated **LangGraph Dev** to monitor and visualize workflow execution
- Enabled **live streaming** to observe real-time message updates
- Implemented **event-driven tracking** to analyze node behavior during conversations
- Link : https://github.com/langchain-ai/langchain-academy/blob/main/module-3/streaming-interruption.ipynb
---  

## Learnings from Module 3 (Course 2)
- Learned how to use breakpoints in LangGraph to pause execution before specific nodes.  
- Understood streaming interruptions for human approval or conditional continuation.  
- Explored real-time event tracking with LangGraph SDK’s streaming API.  
- Learned how to monitor, inspect, and resume executions dynamically.  
- Understood how breakpoints enhance debugging and controlled workflow execution.
    
---

### Changes Implemented in Module 3 (Course 2)
- Added breakpoints before tool nodes for user-controlled execution.  
- Integrated LangGraph SDK to stream and observe live events.  
- Demonstrated pausing and resuming graph execution with user input.  
- Created an interactive workflow showcasing human-in-the-loop decision-making.  
- Enhanced transparency and control using real-time graph monitoring.
- Link: https://github.com/langchain-ai/langchain-academy/blob/main/module-3/breakpoints.ipynb  

---

## Learnings from Module 3 (Course 3)

- Learned to perform state updates after interruptions using human feedback.  
- Understood human-in-the-loop correction for adaptive AI workflows.  
- Created a `human_feedback` node to inject user updates dynamically.  
- Used `interrupt_before` and `update_state()` for mid-run state modification.  
- Learned how checkpointers enable resuming from paused states.  
- Observed improved interactivity and transparency in AI execution.

---

### Changes Implemented in Module 3 (Course 3)

- Added `human_feedback` node for user-driven updates.  
- Configured `interrupt_before` to pause before feedback collection.  
- Enabled state editing using `update_state()` during execution.  
- Implemented checkpointing for safe resumption post-update.  
- Demonstrated resuming execution after applying user feedback.  
- Validated dynamic correction and adaptability in the chess workflow.
- Link: https://github.com/langchain-ai/langchain-academy/blob/main/module-3/edit-state-human-feedback.ipynb

