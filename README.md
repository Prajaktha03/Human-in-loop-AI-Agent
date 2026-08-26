# 🤖 Human-in-the-Loop AI Sales Agent

### What if an AI could write your sales emails — but couldn't send them without your approval?

This project explores that idea by combining AI agents, workflow automation, and human decision-making into one n8n workflow.
The system turns raw lead information into a personalized sales email, pauses for human judgment, and intelligently handles the decision that follows.

### 🧩 The Core Mechanism

The workflow has three intelligent roles:

    Role	                  Responsibility
🧠 Sales Agent        	Creates the first email
👤 Human Reviewer      	Decides whether it is ready
🔧 Revision Agent	      Improves rejected drafts.
