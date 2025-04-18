<p align="center">
  <a href="README.ja.md"><img src="https://img.shields.io/badge/ドキュメント-日本語-white.svg" alt="JA doc"/></a>
  <a href="README.md"><img src="https://img.shields.io/badge/english-document-white.svg" alt="EN doc"></a>
</p>

<p align="center">
  <img src="assets/logo.png" width="200"/>
  <img src="assets/logo2.png" width="200"/>
</p>

<h1 align="center">Claude Hands</h1>

<div align="center">

[![GitHub stars](https://img.shields.io/github/stars/r488it/claude_hands?style=social)](https://github.com/r488it/claude_hands/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

</div>

Claude Hands is a project that recreates Manus implementation using Claude Desktop and MCP (Model Control Protocol).


## Update

- 2025.4.19 Refined Docker setup to support Windows environment.
- 2025.3.29 Browser operation supported.   
- 2025.3.29 ChatGPT Desktop supported. chatgpt_mcp_agent.config.yaml

## Recommended Model
- Claude 3.7 Sonnet
- Claude 3.7 Sonnet think mode

## Demo

https://github.com/user-attachments/assets/615c8973-c117-4012-9111-e44d594d6869

## 🚀 Features

- Pre-configured Docker environment for Claude Code development
- Enhanced information retrieval with Tavily search integration
- Seamless compatibility with Claude Desktop through MCP interfaces
- Powerful graphic recording-style infographic generation capabilities

## Prerequisites

- Docker and Docker Compose
- Claude Desktop application
- Tavily API key

## 🛠 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/r488it/claude_hands.git
cd claude_hands
```

### 2. Configure Environment Variables

Create a `.env` file in the root directory:

```bash
touch .env
```

Add your Tavily API key to the `.env` file:

```
TAVILY_API_KEY=your_tavily_api_key_here
```

### 3. Update Docker Volume Paths

Edit the `docker-compose.yml` file to match your system's paths:

```yaml
volumes:
  - /path/to/your/workspace:/workspace
```

### 4. Start the Services

```bash
docker-compose up -d
```

This command will:
- Pull the required Docker images (if not already available)
- Start the Claude Code and Tavily services
- Make the services available on the configured ports

## Connecting with Claude Desktop

1. Copy the `claude_desktop_config.json` file to your Claude Desktop configuration directory
2. Restart Claude Desktop
3. You can now use the MCP servers through Claude Desktop

## Usage

1. Create a new project
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/01_make_project.png" alt="Create project" width="300" />
</div>

2. Set up your prompt
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/02_set_prompt.png" alt="Set prompt" width="300" />
</div>

3. Add knowledge template (optional)
<div align="center" style="display: flex; gap: 20px;">
    <img src="assets/03_set_knowledge.png" alt="Add knowledge" width="300" />
</div>

## 📚 Additional Documentation
- [Knowledge Base](knowledge.md)
- [Prompt (EN)](prompt.md)
- [Prompt (JA)](prompt.ja.md)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=r488it/claude_hands&type=Date)](https://www.star-history.com/#r488it/claude_hands&Date)
