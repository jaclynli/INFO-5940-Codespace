What I learned from implementing a multi-agent workflow
I learned how to shape each agent’s behavior by writing targeted system-prompt instructions and configuring external tool calls such as the internet search tool. Crafting these prompts helped me learn how to better control and guide the agents’ outputs. For example, the Planner Agent’s output is intentionally structured to serve as the input for the Reviewer Agent. Seeing and understanding this connection taught me how information flows through a multi-agent system and how each agent’s role and tasks depend on the workflow design.

Challenges faced and how I addressed them
First challenge: The Reviewer Agent wasn’t evaluating based on real-time data because my Tavily API key was missing. I noticed, then  registered and added the key to restore internet access.
Another challenge was reformatting and refining the Reviewer Agent’s output so the final plan would be presented more clearly to users at once glance. Initially, I have a brief validation summary and then a  delta List that shows each day’s trip plan with specific corrections and explanations. However, I realized that the output quality and the sequence of the Reviewer Agent’s output wasn’t ideal for a real user as it’s still hard for the audience to quickly identify the final recommended plan. To address this, I updated the system prompt to require the Reviewer Agent to present a clearly structured (ex: Day 1, city& theme) with a finalized itinerary first then followed by the validation summary and the delta list. 

Creative ideas, variations, or design choices
I wanted to make this trip planning agent not only functional, but also friendly and welcoming, providing some emotional values like real trip planners. So in the system prompts, I not only described their tasks but also added descriptive words that defined the agent’s personalities. 



