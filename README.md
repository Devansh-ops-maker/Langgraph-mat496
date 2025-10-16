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
