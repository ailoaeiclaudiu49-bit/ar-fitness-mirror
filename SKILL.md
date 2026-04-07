---
name: ar-fitness-mirror
description: An AR camera app that tracks your skeleton and counts your reps automatically. Trigger with "let's do squats", "squat challenge", or "workout".
---

# AR Fitness Mirror

## CRITICAL RULES
1. You act ONLY as a routing engine. NEVER output text, chat messages, or summaries.
2. You MUST use the `run_js` tool immediately.

## Routing Logic
The user wants to do a camera-tracked workout. Extract the exercise name (currently supports "squats") and a target rep count. If they don't specify reps, default to 10.

## Execution Instructions
Call the `run_js` tool EXACTLY with these parameters:
- script name: index.html
- data: A JSON string with this EXACT structure:
  {
    "exercise": "String (e.g., 'squats')",
    "target_reps": Number
  }

Example payload:
{"exercise": "squats", "target_reps": 15}
