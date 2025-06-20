# Prompt Recommendations

This document provides guidance for crafting effective prompts, drawing from [80,000 Hours' guide on AI skills](https://80000hours.org/agi/guide/skills-ai-makes-valuable/?utm_source=tldrai) and the [Anthropic Cookbook's prompt patterns](https://github.com/anthropics/anthropic-cookbook/tree/main/patterns/agents/prompts).

## Principles for Effective Prompts

- **Be Specific:** Clearly state the task, context, and desired output.
- **Structure Inputs:** Use lists, bullet points, or sections to organize information.
- **Iterate and Refine:** Test prompts and adjust based on results.
- **Provide Examples:** Show desired input-output pairs to guide the model.
- **Set Constraints:** Define length, style, or format requirements.

## Recommended Prompt Patterns

1. **Instructional Prompts**
    - Directly state what you want the AI to do.
    - *Example:*  
      ```
      Summarize the following article in three bullet points.
      ```

2. **Role-based Prompts**
    - Assign a role to the AI for more targeted responses.
    - *Example:*  
      ```
      You are a software engineer. Review this code for security issues.
      ```

3. **Step-by-Step Prompts**
    - Ask the AI to reason through tasks step by step.
    - *Example:*  
      ```
      List the steps required to deploy a web application.
      ```

4. **Few-shot Prompts**
    - Provide examples of correct outputs.
    - *Example:*  
      ```
      Q: What is 2+2?  
      A: 4  
      Q: What is 3+5?  
      A: 8  
      Q: What is 7+6?  
      A: 13
      ```

## Additional Resources

- [80,000 Hours: Skills AI Makes Valuable](https://80000hours.org/agi/guide/skills-ai-makes-valuable/?utm_source=tldrai)
- [Anthropic Cookbook: Prompt Patterns](https://github.com/anthropics/anthropic-cookbook/tree/main/patterns/agents/prompts)

Use these recommendations to improve prompt clarity, reliability, and effectiveness in your projects.
