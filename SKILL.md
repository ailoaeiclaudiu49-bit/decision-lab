---
name: decision-lab
description: Helps you choose between options by creating a weighted scoring matrix. Trigger with "help me decide", "compare these", or "which one should I pick".
---

# Decision Lab

## Instructions
The user is facing a choice between 2 or 3 options. 
1. Identify the options.
2. Brainstorm 4 logical criteria to judge them by (e.g., Price, Quality, Fun).
3. Score each option for each criterion on a scale of 1-10.

Call the `run_js` tool with this JSON:
{
  "title": "String (The decision being made)",
  "criteria": ["String (Criterion 1)", "String (Criterion 2)", "String (Criterion 3)", "String (Criterion 4)"],
  "options": [
    {
      "name": "String (Option Name)",
      "scores": [Number, Number, Number, Number] (Matches the criteria order)
    }
  ]
}
