# 🤖 Human-in-the-Loop AI Sales Agent

### What if an AI could write your sales emails — but couldn't send them without your approval?

This project explores that idea by combining AI agents, workflow automation, and human decision-making into one n8n workflow.
The system turns raw lead information into a personalized sales email, pauses for human judgment, and intelligently handles the decision that follows.

### 🧩 The Core Mechanism

The workflow has three intelligent roles:

| Role | Responsibility |
|---|---|
| 🧠 **Sales Agent** | Creates the first email |
| 👤 **Human Reviewer** | Decides whether it is ready |
| 🔧 **Revision Agent** | Improves rejected drafts |

### 📨 From Lead to Conversation

A lead provides basic information through an n8n form:

Name
Email
Company
Budget
Requirement
The information is recorded in Google Sheets and becomes the context for the AI.
The Sales Agent then transforms those structured details into a personalized email rather than relying on a fixed template.

### 🔍 The Interesting Part: Rejection

Most automation systems treat rejection as the end.
This workflow treats rejection as input.
When a reviewer rejects an email, the system doesn't simply stop.
The rejected draft is handed to a separate Revision Agent, which produces an improved version for another review.
**Conceptually:**

```text
Draft
  │
  ▼
Human Judgment
  │
  ├── ✓ Good enough → Delivery
  │
  └── ✕ Not good enough
              │
              ▼
         AI Revision
              │
              ▼
        Human Judgment
