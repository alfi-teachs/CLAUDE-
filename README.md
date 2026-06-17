# CLAUDE-
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

| Model         | Best For                      | Use Cases                                                        |
| ------------- | ----------------------------- | ---------------------------------------------------------------- |
| Claude Opus   | Highest intelligence          | Complex reasoning, research, advanced coding, data analysis      |
| Claude Sonnet | Balanced performance and cost | Chatbots, coding, content creation, business applications        |
| Claude Haiku  | Fastest and cheapest          | Quick responses, summarization, classification, customer support |

### Quick Rule

* **Opus** → Most capable
* **Sonnet** → Best balance of speed, cost, and intelligence
* **Haiku** → Fastest and lowest cost

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
