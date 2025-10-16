# Langgraph Project

**Author:** Devansh Singh (2410110755)

---

## Learnings from Module 1(Course 1)

From this course, we learned how to make a simple graph.  
We understood the concept of **states**, which hold the data passed between nodes. It ensures every function knows what kind of data it is receiving and returning.  

Each **node** is a small function that takes the current state, modifies it, and returns the updated version.  
**Edges** tell the graph how the nodes are connected.  
The **StateGraph** class helps in building this pipeline and managing the flow between nodes.

---

## Changes Implemented in Module 1 (Course 1)

I created my own version of the graph with **five nodes**, representing a simple flow of sentences.  
Instead of using conditional edges, I implemented a **linear sequence of nodes**, where each node updates the text state.  
The final output forms a smooth message by passing the state sequentially through all nodes until reaching the `END` node.

---

## Learnings from Module 1 (Course 2)

We learned how to create **messages** that capture different roles, such as `AIMessage` and `HumanMessage`, and how to use them in chat models.  
We understood that chat models can take multiple messages as input and generate a follow-up response based on the conversation history.  
We also learned how to **bind tools with an LLM**, allowing the model to perform specific tasks programmatically.  
Additionally, we explored how to use **messages as the graph state** and how to integrate **MessageState** with our graph for dynamic conversation flows.

---

## Changes Implemented in Module 1 (Course 2)

We implemented a **coding-related conversation** graph where the user could ask programming questions, and the LLM would respond contextually.  
We also created a **factorial tool** and bound it to the LLM, allowing the graph to perform computations dynamically based on user input.  
These changes made the graph more **interactive and versatile**, enabling it to handle coding queries and execute functions while maintaining conversation context.

---
