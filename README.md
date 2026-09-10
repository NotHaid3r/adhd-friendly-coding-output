# ADHD-Friendly Coding Output

> A skill for coding agents that stops useful answers from getting buried in walls of text.

Coding agents can be incredibly useful — but their responses can sometimes be harder to use than the actual code.

Long explanations.  
Huge investigation logs.  
Important errors buried halfway down.  
Five paragraphs before telling you what actually happened.

This skill fixes that.

## 🎯 The Goal

Make coding-agent output follow one simple principle:

**Scan → Understand → Act**

You should be able to look at a response and immediately know:

- What happened?
- Did it work?
- What changed?
- Is anything broken?
- What do I do next?

No digging required.

---

## ✨ What It Changes

The skill encourages coding agents to:

- Put the answer first
- Keep responses short and scannable
- Use clear headings
- Prefer bullets over walls of text
- Put commands in copyable code blocks
- Clearly identify errors
- Clearly show what changed
- Clearly show test results
- Give one obvious next step
- Avoid unnecessary explanations
- Avoid repeating the same information
- Avoid dumping investigation logs
- Avoid narrating every step of their reasoning

---

## ❌ Before

A typical coding-agent response might look like:

> I started by investigating the repository structure and examining the package configuration. I then looked through the source files to determine how the authentication system was implemented. After that I checked the middleware configuration and compared it against the current session handling implementation. There appeared to be several possible causes...
>
> After investigating several files and testing different possibilities...
>
> The actual problem is that the authentication middleware runs before the session middleware.
>
> You should probably move it...
>
> Also, there are some other things you may want to consider...

The answer is there.

But you had to **hunt for it**.

---

## ✅ After

With ADHD-Friendly Output:

### ✅ Fixed

The authentication middleware was running before the session middleware.

### 🔧 Changed

- Moved session initialization before authentication
- Added session validation
- Updated `src/middleware/auth.ts`

### 🧪 Tested

```bash
npm test