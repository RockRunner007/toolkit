# A Software Engineer Toolkit

This toolkit is designed for software engineers who care deeply about building effective, maintainable, and impactful solutions. It provides practical resources, such as persona-driven prompt templates, to help you communicate more effectively with AI tools and stakeholders. Whether you're advocating for best practices, navigating organizational dynamics, or seeking to improve your workflow, this toolkit offers guidance and examples tailored to real-world engineering challenges.

## Using frameworks for Effective Prompts

To create effective prompts, consider using a structured framework that helps clarify your request. Here are some key principles and a recommended format:

- Use a prompt framework to structure your request:
  - **Task:** What should the AI do?
  - **Context:** What background or details are relevant?
  - **Examples:** Provide sample inputs and outputs if possible.
  - **Persona:** Specify a role or perspective for the AI.
  - **Format:** Indicate the desired output structure (e.g., list, table, paragraph).
  - **Tone:** Set the style or mood (e.g., formal, friendly, concise).

## Using Personas to Influence AI Prompts

This toolkit includes ready-to-use personas in the [`personas`](personas) directory. Each persona models a typical stakeholder or attitude you might face when discussing technical solutions. Reference a persona by name in your prompt to shape AI responses.

- **boss**: Focuses on management concerns like cost, timelines, and risk.
- **burned**: Skeptical due to negative past experiences with similar solutions.
- **cynic**: Challenges new ideas to appear knowledgeable or maintain the status quo.
- **herd**: Follows established practices and responds well to clear direction.
- **irrational**: Opposes change for unstated, non-rational reasons; best managed, not convinced.
- **time_crunched**: Overwhelmed by workload; needs to see clear time-saving benefits.
- **uninformed**: Lacks awareness of best practices; easy to inform but may be skeptical.

To use a persona, specify its name and relevant traits in your prompt. For example:

```
As a "boss" persona, create a scrum ticket that outlines the need for a new feature to improve team collaboration.
```

You can also combine multiple persona attributes to achieve the desired tone and expertise in AI responses.

**Tip:** For more accurate results, you can copy the contents of the relevant persona file from the [`personas`](personas) directory and include it directly in your prompt. This gives the AI full context about the persona's background and motivations.
