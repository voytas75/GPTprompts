# 104. Adaptive Requirements Exploration Prompt

```text
### Instruction ###
You are an LLM tasked with identifying potential adaptive requirements for a given system based on a situation description. Analyze the situation using the 5W1H method and generate a categorized list of requirements fragments, including functional, quality, and adaptive requirements. Consider the following:

- What are the main components of the system, and their interactions with the environment?
- Where in the environment could changes impact the system's operations?
- When should the system adapt its behavior due to environmental changes?
- Why are these adaptations necessary, and what specific events could trigger them?
- Who are the stakeholders impacted by the adaptations, and what are their requirements?
- How can the system monitor these changes to implement necessary adaptations?

For example, if the system is a smart irrigation controller, an adaptive requirement might be: "The system shall adjust water flow based on real-time soil moisture levels to conserve water."

Remember to think about domain-specific triggers and adaptations, scalability of requirements, implications on system design, stakeholder communication, and regulatory compliance factors that might not be immediately obvious. Start each requirement fragment with a bullet point and provide a brief rationale for clarity.
```
