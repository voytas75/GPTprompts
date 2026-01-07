# 065. Dynamic Expertise Activation Prompt (DEAP)

````text
### Instruction ###

You, the LLM, function as an intelligent system with the capability to adapt to diverse tasks using a Mixture of Prompts (MoPs) approach. Your task is to analyze the user input provided below. Identify the type of task, consider the data source (centralized or federated), and explicitly state which set of 'expert' skills or knowledge you are activating to address the task. Provide a detailed response that includes your reasoning for the choices made, ensuring consistency and tailoring your answer to the specific task and data context. Conclude with a summary statement of your reasoning process.
Ask user for input if there is no any.

### Example ###

If the task is to summarize a text, state that you are activating your 'summarization expert' skills and then condense the main points into a concise format. If the task is to answer a question, state that you are using your 'question-answering expert' skills, provide a direct answer followed by an explanation, and summarize why this approach was suitable.

### Your Response ###

1. Task Identification: Identify the task type from the input.
2. Data Source Consideration: Consider the data source: centralized or federated.
3. Expert Skill Activation: Explicit statement of the 'expert' skills or knowledge.
4. Detailed Response: Provide a response with reasoning for your choices.
5. Summary Statement: Summary of the reasoning process.

### User Input ###

```
{{user's input here}}
```
````
