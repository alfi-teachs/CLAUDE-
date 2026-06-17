# CLAUDE

## What is Claude?

Claude is an AI assistant designed to be more than just a chatbot. It acts as a thinking partner, helping users reason through problems, generate ideas, write content, analyze information, and complete complex tasks.

---

# Claude Architecture (Three Layers)

## 1. Primitive Layer

Core AI capabilities:

* Understand language
* Generate responses
* Reason and solve problems
* Process text and images

## 2. Infrastructure Layer

Systems that support Claude:

* Model hosting
* Compute resources
* Scaling
* Security
* Data processing

## 3. Controls Layer

Safety and governance mechanisms:

* Safety filters
* Guardrails
* Permission controls
* Policy enforcement
* Monitoring

---

# Using Claude API

## Step 1: Get an API Key

1. Visit Claude Platform
2. Create an account
3. Purchase API credits
4. Generate an API Key
5. Copy the key securely

## Step 2: Store the API Key

Create a `.env.local` file:

```env
ANTHROPIC_API_KEY=your_api_key_here
```

This keeps the API key out of your source code and version control.

---

# Install Claude SDK

```bash
npm install @anthropic-ai/sdk
```

---

# Requirements for an API Request

| Component     | Description                                  |
| ------------- | -------------------------------------------- |
| Model         | Claude model to use (e.g., Claude Sonnet)    |
| Max Tokens    | Maximum number of tokens Claude can generate |
| Messages      | Conversation history sent to Claude          |
| System Prompt | Instructions defining Claude's behavior      |

---

# Example API Request

```javascript
const response = await anthropic.messages.create({
  model: "claude-sonnet-4",
  max_tokens: 1024,

  system: "You are a helpful assistant.",

  messages: [
    {
      role: "user",
      content: "Hello Claude"
    }
  ]
});
```

---

# Content Types Claude Can Process

Claude can process:

* Text
* Images
* Documents (PDFs)
* Code
* Structured Data

---

# Choose a Model
## Choose a Model

| Model         | Best For                      | Use Cases                                                        |
| ------------- | ----------------------------- | ---------------------------------------------------------------- |
| Claude Opus   | Highest intelligence          | Complex reasoning, research, advanced coding, data analysis      |
| Claude Sonnet | Balanced performance and cost | Chatbots, coding, content creation, business applications        |
| Claude Haiku  | Fastest and cheapest          | Quick responses, summarization, classification, customer support |
| Claude Fable  | Long-running AI agents        | Autonomous workflows, multi-step tasks, agentic applications     |
| Claude Mythos | Knowledge-intensive reasoning | Deep research, large-scale analysis, complex decision making     |

### Quick Rule

* **Opus** → Most capable general-purpose model
* **Sonnet** → Best balance of speed, cost, and intelligence
* **Haiku** → Fastest and lowest cost
* **Fable** → Best for long-running autonomous agents
* **Mythos** → Best for deep knowledge and complex reasoning
---

# Quick Flow

```text
Create Account
      ↓
Purchase Credits
      ↓
Generate API Key
      ↓
Store in .env.local
      ↓
Install SDK
      ↓
Choose Model
      ↓
Set max_tokens
      ↓
Add system prompt
      ↓
Add messages
      ↓
Send API Request
      ↓
Receive Response
```

## Choose a Model

| Model         | Best For                      | Use Cases                                                        |
| ------------- | ----------------------------- | ---------------------------------------------------------------- |
| Claude Opus   | Highest intelligence          | Complex reasoning, research, advanced coding, data analysis      |
| Claude Sonnet | Balanced performance and cost | Chatbots, coding, content creation, business applications        |
| Claude Haiku  | Fastest and cheapest          | Quick responses, summarization, classification, customer support |

### Quick Rule

* **Opus** → Most capable
* **Sonnet** → Best balance of speed, cost, and intelligence
* **Haiku** → Fastest and lowest cost

```python
models = ["claude-haiku-4-5", "claude-sonnet-4-6", "claude-opus-4-7"]

for model in models:
    response = client.messages.create(
        model=model,
        max_tokens=300,
        messages=[
            {
                "role": "user",
                "content": prompt
            }
        ],
    )

    print(model, response.usage)
```
## What is an Agent?

An **Agent** is Claude that can work on its own. It receives a task, uses tools, and keeps working until the task is finished.

### Agent Steps

1. User gives a task.
2. Claude chooses a tool.
3. Tool runs and returns a result.
4. Claude uses the result.
5. Repeat until the task is complete.
-------------------------------------------------------------------------------------------------------------------------------
## What are Tools?

Tools help Claude perform actions and access external systems.

* You create the tool.
* Claude decides when to use it.
* Your code runs the tool.
* The result is sent back to Claude.

### Example

User: "What is the weather today?"

Claude → Uses a weather tool
Tool → Gets weather data
Claude → Returns the answer

### A Tool Has

* **Name** – Tool name
* **Description** – What the tool does
* **Input Schema** – Information the tool needs

### Key Point

Tools let Claude interact with APIs, databases, files, and other systems.

