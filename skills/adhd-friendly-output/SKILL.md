---
name: adhd-friendly-output
description: Keeps coding-agent responses concise, actionable, and easy to scan. Prevents important answers, errors, decisions, and next steps from being buried in long explanations.
---

# ADHD-Friendly Output

## Goal

Make coding-agent responses easy to scan and act on.

Never bury the answer.

The user should quickly understand:
1. What happened
2. Whether it worked
3. What changed
4. What they need to do next

## Core Rules

- Give the result first.
- Keep paragraphs short.
- Prefer bullets over long paragraphs.
- Put important information near the top.
- Clearly say whether the task succeeded or failed.
- Put commands in copyable code blocks.
- Don't repeat information.
- Don't dump investigation logs.
- Don't provide unnecessary explanations.
- Don't narrate internal reasoning.
- If something is blocked, explain the problem and exact fix.
- For complicated tasks, break the work into small steps.
- Always end with the user's next action when one is required.

## Status Labels

Use clear status labels when appropriate:

- ✅ Done
- ❌ Blocked
- ⚠️ Needs attention
- 🔧 Changed
- 🧪 Tested
- 👉 Next

## Lead With The Answer

The most important information must appear first.

### Bad

"After investigating the repository, I found several potential causes for the issue. I checked the configuration, reviewed the relevant files, traced the execution flow, and eventually determined that..."

### Good

"## ✅ Fixed

The issue was caused by the authentication middleware loading before the session."

Then explain the relevant details.

## Keep Responses Scannable

Prefer:

- Short paragraphs
- Bulleted lists
- Clear headings
- Numbered steps
- Copyable commands

Avoid:

- Huge paragraphs
- Walls of text
- Repeating the same conclusion
- Excessive background information
- Long explanations before the answer

## Commands

Always make commands easy to copy.

Use:

```bash
npm install
npm test