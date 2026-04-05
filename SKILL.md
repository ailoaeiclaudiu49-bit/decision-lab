---
name: decision-lab
description: Helps you choose between options by creating a weighted scoring matrix. Trigger with "help me decide", "compare these", or "which one should I pick".
---

# Decision Lab

## CRITICAL INSTRUCTIONS
- DO NOT summarize the results or options in a chat message.
- YOUR ONLY GOAL is to call the `run_js` tool.
- If you do not call the tool, the user cannot see their interactive matrix.

## Task Steps
The user is facing a choice between 2 or 3 specific options.
1. Identify the options they are comparing.
2. Brainstorm 4 logical, distinct criteria to judge them by (e.g., Taste, Texture, Price, Prep Time).
3. Score each option for each criterion on a scale of 1 to 10 (10 being the best).

## Tool Parameters
Call the `run_js` tool with the EXACT following parameters:
- script name: index.html (CRITICAL: You MUST use exactly "index.html". Do not use the skill name.)
- data: A JSON string following this structure:
  {
    "title": "String (e.g., 'Choosing a New Smartphone')",
    "criteria": ["String (Crit 1)", "String (Crit 2)", "String (Crit 3)", "String (Crit 4)"],
    "options": [
      {
        "name": "String (Option Name)",
        "scores": [Number, Number, Number, Number]
      }
    ]
  }

Example:
{"title": "Ice Cream Choice", "criteria": ["Taste", "Texture", "Price", "Flavor Profile"], "options": [{"name": "Chocolate", "scores": [9, 8, 5, 10]}, {"name": "Vanilla", "scores": [8, 9, 6, 7]}]}
