# Grok 4 CLI

A terminal-based LLM tool using xAI's Grok 4 model via their API.

## Setup

### 1. Get API Keys
- **xAI API Key**: Get your API key from https://x.ai/api
- **Composio API Key**: Get your API key from https://composio.dev

### 2. Install Dependencies
```bash
pip install -r requirements.txt
pip install -e .
```

### 3. Configure API Keys

#### Option A: Using .env file (Recommended)
Create a `.env` file in the project root:
```env
XAI_API_KEY=your-xai-api-key-here
COMPOSIO_API_KEY=your-composio-api-key-here
```

#### Option B: Environment Variables
```bash
export XAI_API_KEY=your-xai-api-key-here
export COMPOSIO_API_KEY=your-composio-api-key-here
```

#### Option C: Command Line
```bash
grok_cli --api-key YOUR_XAI_KEY
# (Still requires COMPOSIO_API_KEY environment variable)
```

### 4. Run the CLI
```bash
grok_cli
```

Or with a specific API key:
```bash
grok_cli --api-key YOUR_XAI_KEY
```

## Development Mode
Use OpenAI's cheaper GPT-3.5-turbo model for development:
```bash
grok_cli --dev
# Requires OPENAI_API_KEY environment variable
```

## Usage
- Enter prompts at "You: ".
- Type "exit" to quit.
- Conversation history is maintained.
- The CLI has access to file tools via Composio integration.
