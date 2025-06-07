# toolkit

Helper for Engineers

## Using Personas to Influence AI Prompts

This project includes a set of predefined personas located in the [`personas`](personas) directory. Each persona represents a common stakeholder or attitude you may encounter when proposing technical solutions. You can reference these personas by name to guide AI behavior or tailor responses. The available personas are:

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
